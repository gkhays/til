# Shebang! Run Single File Java as Script

Write a script in Java and run it as a shebang file.

> Shebang support is not natively available in Windows

```java
#!/user/bin/java --source 11
import java.io.File;
public class CanonicalTest {
    public static void main(String[] args) throws Exception {
        System.out.println(new File("").getCanonicalPath());
    }
}
```

```bash
./canonicalPath
/home/ghays/poc/java-shebang
```

## References

1. [Single File Source Code with Java 11](https://medium.com/oracledevs/single-file-source-code-with-java-11-74d1a4c3d31)
1. [JEP 330: Launch Single-File Source-Code Programs](https://openjdk.java.net/jeps/330)
1. [Shebang script files with Java and Docker](https://thepracticaldeveloper.com/shebang-script-java/)
