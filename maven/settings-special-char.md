# Special Characters in Maven Settings

Upon changing my password, I observed the following error.

```
$ mvn package
[ERROR] Error executing Maven.
[ERROR] 1 problem was encountered while building the effective settings
[FATAL] Non-parseable settings C:\Users\haysg\.m2\settings.xml: entity reference name can not contain character <' (position: START_TAG seen ...<password>Blorto>Snorto<... @330:27)  @ C:\Users\haysg\.m2\settings.xml, line 330, column 27
```

Mapping of escape characters.

| Symbol | Escape character |
| ------ | ---------------- |
| <      | \&lt;            |
| >      | \&gt;            |
| &      | \&amp;           |
| '      | \&apos;          |
| "      | \&quot;          |

## References

1. [Maven Escape Special Characters](https://bigdata-etl.com/maven-settingsxml-password-special-characters/)
