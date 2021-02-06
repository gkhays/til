# Add Swagger Documentation to Dropwizard

Update the YAML configuration file.

```yml
swagger:
  resourcePackage: org.gkh.rest.resources
  uriPrefix: /api/v1
  title: "REST API"
  version: v1
  description: "REST API endpoints"
```

References

1. [Augmenting Dropwizard with Swagger and Rollbar](https://www.reonomy.com/blog/post/augmenting-dropwizard-with-swagger)
1. [Serving Static Assets with DropWizard](https://spin.atomicobject.com/2014/10/11/serving-static-assets-with-dropwizard/)
1. [Swagger Bundle Configuration](https://github.com/smoketurner/dropwizard-swagger/blob/master/src/main/java/io/federecio/dropwizard/swagger/SwaggerBundleConfiguration.java)
1. [how to change the default Controller Name in Swagger Spring](https://kalliphant.com/swagger-spring-rest-controllername-change/)
1. [Dropwizard Swagger](https://github.com/smoketurner/dropwizard-swagger)
1. [Automatic Swagger documentation for Dropwizard using Maven](https://itazura.io/automatic-swagger-integration-for-dropwizard-using-maven/)
