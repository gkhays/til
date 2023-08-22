# Set Execute Permission in Maven

How to set the execute bit on a script employed within a Maven build. **Note**: This is geared towards Linux and other "\*nix" systems.

## Maven Exec Plugin

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.codehaus.mojo</groupId>
            <artifactId>exec-maven-plugin</artifactId>
            <version>...</version>
            <executions>
                <execution>
                    <id>set-script-permissions</id>
                    <phase>prepare-package</phase>
                    <goals>
                        <goal>exec</goal>
                    </goals>
                    <configuration>
                        <executable>chmod</executable>
                        <arguments>
                            <argument>+x</argument>
                            <argument>path/to/your/script.sh</argument>
                        </arguments>
                    </configuration>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

## Maven Antrun Plugin

This one feels "Ansible-ish" to me.

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-antrun-plugin</artifactId>
            <version>...</version>
            <executions>
                <execution>
                    <phase>prepare-package</phase>
                    <goals>
                        <goal>run</goal>
                    </goals>
                    <configuration>
                        <tasks>
                            <chmod file="path/to/your/script.sh" perm="ugo+x"/>
                        </tasks>
                    </configuration>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```
