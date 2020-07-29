# Database Transactions in Non-Jersey Resources

Dropwizard provides an annotation or aspect, `@UnitOfWork`, that wraps a Jersey resource method in a Hibernate transaction. Unfortunately this is not available for other modules such as commands.

The [Transactional Resource Methods Outside Jersey Resources](https://www.dropwizard.io/en/latest/manual/hibernate.html) section of the Dropwizard Hibernate documentation mentions the `UnitOfWorkAwareProxyFactory` but is not clear how to actually use it.

The example below shows how to enable transactional methods in a Dropwizard command. The key is to extend `EnvironmentCommand` instead of `Command` or `ConfiguredCommand` as would typically be done.

The other trick is to create an accessor method in your application in order to retrieve the `HibernateBundle`, e.g.

```
public HibernateBundle<YourConfiguration> getHibernateBundle() {
    return this.hibernate;
}
```

Finally, create a `UnitOfWorkAwareProxyFactory` using your DAO object.

```
DAOProxy proxy = new UnitOfWorkAwareProxyFactory(hibernate)
                        .create(DAOProxy.class, MyDAO.class, myDao);
```

**Note**: where we wish transactions, we have annotated the methods with `@UnitOfWork`.

Here is the proxy we will create.

```
public class DAOProxy {

    private MyDAO myDao;

    public DAOProxy(MyDAO myDao) {
        this.myDao = myDao;
    }

    @UnitOfWork
    public Credential createWrapper(MyEntity) {
        return myDao.create(MyEntity);
    }

    @UnitOfWork
    public List<MyEntity> findAllWrapper() {
        return myDao.findAll();
    }

}
```

## References

1. [@UnitOfWork usable outside of Jersey Resource classes #1240](https://github.com/dropwizard/dropwizard/issues/1240)
1. [Support `@UnitOfWork` outside of Jersey resources #1361](https://github.com/dropwizard/dropwizard/pull/1361)
1. [Using Hibernate DAOs in DropWizard Tasks](https://spin.atomicobject.com/2015/02/03/dropwizard-hibernate-dao/)
1. [Managed Session Transaction Provider (Gist)](https://gist.github.com/vvondra/1dbcd62306e40fa47294)

Related

[Managing environment lifecycles for Dropwizard Commands](https://sadique.io/blog/2019/07/28/managing-environment-lifecycles-for-dropwizard-commands/)
