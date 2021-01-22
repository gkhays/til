# Convert Hex to Base64

```java
import org.apache.commons.codec.binary.Base64;
import org.apache.commons.codec.binary.Hex;

byte[] decodedHex = Hex.decodeHex(hex);
byte[] encodedHexB64 = Base64.encodeBase64(decodedHex);
```

## References

1. [how to convert hex to base64](https://stackoverflow.com/a/7372374/6146580)
1. [Apache Commons Codec](https://commons.apache.org/proper/commons-codec/)
