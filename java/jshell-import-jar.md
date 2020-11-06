# Import External Library in JShell

```java
jshell> /env --class-path C:\Users\ghays\.m2\repository\javax\mail\mail\1.4.7\mail-1.4.7.jar
|  Setting new options and restoring state.

jshell> import javax.mail.internet.InternetAddress

jshell> InternetAddress from = new InternetAddress("til@acme.org");
from ==> til@acme.org
```

## References

1. [How to import external libraries in JShell in Java 9?](https://www.tutorialspoint.com/how-to-import-external-libraries-in-jshell-in-java-9)
