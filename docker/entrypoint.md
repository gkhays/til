# Override the Entry Point

The entry point may be overridden with the `--entrypoint` switch in a `docker run` invocation but the mistake I made was to immediately follow it with arguments. Those actually go last.

> ...the documentation clearly states that the ENTRYPOINT only specifies the executable to run, when the container starts.

```bash
docker run -d \
  --name h2-gui --rm \
  -v "${PWD}/data:/data" \
  -p "8082:8082" \
  --entrypoint "java" \
  h2-docker:latest \
  -cp bridge-agent.jar org.h2.tools.GUIConsole -webAllowOthers
```

You can do the same thing with Docker Compose. Although there is a slight change; the java VM arguments stay with the entry point. Otherwise:

```bash
yaml: line 7: did not find expected node content
```

```yml
version: "2.1"
services:
  h2-ui:
    image: h2-docker:latest
    entrypoint: ["java", "-cp", "h2.jar"]
    command: ["org.h2.tools.GUIConsole", "-webAllowOthers"]
    volumes:
      - ./data:/data
    ports:
      - "8082:8082"
volumes:
  data:
```

## References

1. [How to properly override the ENTRYPOINT using docker run](https://oprearocks.medium.com/how-to-properly-override-the-entrypoint-using-docker-run-2e081e5feb9d))
