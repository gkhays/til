# Add Classpath to Shaded JAR

If you want to use dependencies from another JAR, create a class path manifest entry in the shaded JAR.

```xml
<transformers>
	<transformer implementation="org.apache.maven.plugins.shade.resource.ServicesResourceTransformer" />
	<transformer implementation="org.apache.maven.plugins.shade.resource.ManifestResourceTransformer">
		<mainClass>org.gkh.App</mainClass>
		<manifestEntries>
			<Class-Path>ojdbc8.jar</Class-Path>
		</manifestEntries>
	</transformer>
</transformers>
```

The manifest is as follows.

```
Manifest-Version: 1.0
Built-By: gkh
Class-Path: ojdbc8.jar
Created-By: Apache Maven 3.6.2
Build-Jdk: 1.8.0_232
Main-Class: org.gkh.App
```

## References

1. [How to set manifest class-path in maven shade plugin?](https://stackoverflow.com/questions/17242945/how-to-set-manifest-class-path-in-maven-shade-plugin/17891813#17891813)
1. [Adding Classes to the JAR File's Classpath](https://docs.oracle.com/javase/tutorial/deployment/jar/downman.html)
1. [Apache Maven Shade Plugin > Executable JAR](https://maven.apache.org/plugins/maven-shade-plugin/examples/executable-jar.html)
