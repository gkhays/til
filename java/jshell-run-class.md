# Execute a Java Class with JShell

The `JShell REPL` is useful beyond testing snippets. It is possible to load classes and use them.

```bash
jshell TestClass.java
```

Then

```java
jshell> /list
jshell> TestClass.main(null)
jshell> /exit
```

## References

1. [JShell: A Comprehensive Guide to the Java REPL](https://www.infoq.com/articles/jshell-java-repl/)
1. [Java Platform, Standard Edition Java Shell User’s Guide](https://docs.oracle.com/javase/9/jshell/introduction-jshell.htm#JSHEL-GUID-630F27C8-1195-4989-9F6B-2C51D46F52C8)
