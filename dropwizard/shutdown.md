# Shutdown Options for Dropwizard

Terminating Dropwizard with `Ctrl + C` is perfectly adequate for development and early testing but may not be robust enough going forward.

The [accepted answer](https://stackoverflow.com/a/26211361/6146580) in the Stack Overflow article suggests relying on `kill -SIGINT <pid>` which may be sufficient for most instances. However, I tend to like the `Admin Task` approach.

```java
import io.dropwizard.servlets.tasks.Task;

public class ShutdownTask extends Task {

  public ShutdownTask() {
    super("shutdown"); // the task name, used in the endpoint to execute it
  }

  public void execute(
    ImmutableMultimap<String, String> immutableMultimap,
    PrintWriter printWriter
  ) throws Exception {
    // kill the process asynchronously with some nominal delay
    // to allow the task http response to be sent
    new Timer().schedule(new TimerTask() {
      public void run() {
        // any custom logging / logic here prior to shutdown
        System.exit(0);
      }
    }, 5000);
  }
}
```

## Docker

We may wish to investiatge options for terminating a container workload. In what circumstance would `docker stop` or `docker-compose down` not be enough?

## References

1. [How to shutdown dropwizard application?](https://stackoverflow.com/a/43463781/6146580)
1. [Jetty - Stop a Jetty Server by Command](https://eureka.ykyuen.info/2010/07/26/jetty-stop-a-jetty-server-by-command/)
