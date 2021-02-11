# Get URI Information

```java
@Context
private UriInfo info;

@GET
public response myGetMethod() {
    String baseUril = info.getBaseUri().toASCIIString();
}
```

The `UriInfo` interface also specifies methods to get the path, request URI, and query parameters.

Other uses of `@Context`.

```java
public Response test(@Context HttpServletRequest request) {
    String authInfo = request.getHeader("Authorization")
}
```

## References

1. [JAX-RS @Context tutorial](https://zetcode.com/jersey/context/)
