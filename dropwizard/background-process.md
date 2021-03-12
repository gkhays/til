# Run a Background Process in Dropwizard

Create a managed object.

```java
public class ManagedObject implements Managed {
    private final ExcutorService executor = Executors.newCachedThreadPool();

    @Override
    public void start() {
        executor.execute(() -> {
            Thread t = new Thread(() -> {
                System.out.println("Hi, I'm a thred!");
                Thread.sleep(1000);
            });
            t.start();
        });
    }

    @Override
    public void stop() {
        executor.shutdownNow();
    }
}
```

In the application class, add a lifecycle to the `run` method.

```java
@Override
  public void run(AppConfiguration configuration, Environment environment) throws Exception {
    environment.lifecycle().manage(new ManagedObject());
  }
```

## References

1. [Managing environment lifecycles for Dropwizard Commands](https://sadique.io/blog/2019/07/28/managing-environment-lifecycles-for-dropwizard-commands/)
1. [Running Background Tasks In DropWizard with Guava](https://kountanis.com/2015/02/13/running-background-tasks-in-dropwizard-with-guava/)
1. [Managed Objects](https://www.dropwizard.io/en/latest/manual/core.html#managed-objects)
