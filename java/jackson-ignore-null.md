# Ignore Null Values with Jackson

I didn't actually learn this today but had to re-learn it! It should have been added to a TIL the first time I figured it out!

```java
ObjectMapper mapper = Jackson.newObjectMapper();
mapper.setSerializationInclusion(Include.NON_NULL);
```

It is also possible at the field level.

```java
@JsonInclude(Include.NON_NULL)
private String stringValue;
```

## References

1. [How to tell Jackson to ignore a field during serialization if its value is null?](https://stackoverflow.com/a/11761975/6146580)
1. [Jackson serialization: ignore empty values (or null)](https://stackoverflow.com/a/16089705/6146580)
1. [Jackson Annotations](https://github.com/FasterXML/jackson-annotations/wiki/Jackson-Annotations)
