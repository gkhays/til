# Use Jackson to Deserialize an Array of Objects

```java
List<MyClass> myObjects = mapper.readValue(jsonInput, new TypeReference<List<MyClass>>(){});
```

Or

```java
List<MyClass> myObjects = mapper.readValue(jsonInput, mapper.getTypeFactory()
        .constructCollectionType(List.class, MyClass.class));
```

## References

[How to use Jackson to deserialise an array of objects](https://stackoverflow.com/a/6349488/6146580)
