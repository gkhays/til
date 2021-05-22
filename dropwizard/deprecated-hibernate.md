# Update Deprecated API Reference

In Dropwizard, I am using the built-in `criteria()` method in `AbstractDAO` but keep getting the following warning.

```
org.hibernate.orm.deprecation: HHH90000022: Hibernate's legacy org.hibernate.Criteria API is deprecated; use the JPA javax.persistence.criteria.CriteriaQuery instead
```

So I first looked for an issue in the Dropwizard repo and quickly found one; see issue [#2259](https://github.com/dropwizard/dropwizard/issues/2259). The issue and the warning itself both suggest `javax.persistence.criteria.CriteriaQuery`.

```java
CriteriaBuilder builder = currentSession().getCriteriaBuilder();
CriteriaQuery<Device> cq = criteriaQuery();
Root<Device> c = cq.from(Device.class);
ParameterExpression<String> p = builder.parameter(String.class);
cq.select(c).where(builder.equal(c.get("uniqueId"), p));

TypedQuery<Device> query = currentSession().createQuery(cq);
query.setParameter(p, uniqueId);
return query.getResultList();
```

## References

1. [Update AbstractDAO to use JPA CriteriaQuery API #2259](https://github.com/dropwizard/dropwizard/issues/2259)
1. [JPA Criteria API Queries](https://www.objectdb.com/java/jpa/query/criteria)
1. [JPA Criteria Queries](https://www.baeldung.com/hibernate-criteria-queries)
