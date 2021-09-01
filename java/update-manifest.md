## Update Manifest inside JAR

Create a file, `manifest-attributes.txt`, and add new properties, e.g.

```
Class-Path: additional.jar
```

Then

```bash
jar umf manifest-attributes.txt test.jar
```

If the JAR file is in a container, then copy `manifest-attributes.txt` into a volume.

```bash
docker exec my-container jar umf /bindmount/manifest-attributes.txt test.jar
```

## References

1. [How to update the manifest file in a JAR file](https://nexaweb.jira.com/wiki/spaces/DevCenter/pages/110493703/How+to+update+the+manifest+file+in+a+JAR+file)
1. [Updating a JAR File](https://docs.oracle.com/javase/tutorial/deployment/jar/update.html)
