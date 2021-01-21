# Hide Password in Command Line Argument using Argparse4j

Since [Argparse4j](https://github.com/argparse4j/argparse4j) is a port of Python argparse it supports most expected features, including `getpass()` for password handling. In the case of `argparse4j` it is implemted by the [ArgumentAction](https://argparse4j.github.io/usage.html#custom-actions) interface.

```bash
java App -p
Enter password>
You entered: amazing
```

```java
Subparser subparser;
subparser.addArgument("-p", "--password").action(new PasswordAction());
```

```java
class PasswordAction implements ArgumentAction {

    @Override
    public void run(ArgumentParser parser, Argument arg, Map<String, Object> attrs, String flag, Object value)
            throws ArgumentParserException {
        Console console = System.console();
        value = new String(console.readPassword("%s>", "Enter password"));
        System.out.println("You entered: " + value); // Only for testing!
    }

    @Override
    public void onAttach(Argument arg) {

    }

    @Override
    public boolean consumeArgument() {
        return true;
    }
}
```

## References

1. [Argparse4j Custom Actions](https://argparse4j.github.io/usage.html#custom-actions)
1. [Interface ArgumentAction](https://argparse4j.github.io/apidocs/net/sourceforge/argparse4j/inf/ArgumentAction.html) (JavaDoc)
1. [How to mask a password](https://gist.github.com/gkhays/2bebe536259344779518) (Gist)
1. [Masking password input from the console : Java](https://stackoverflow.com/a/8138549/6146580)
1. [Class Console](https://docs.oracle.com/javase/8/docs/api/java/io/Console.html)
1. [Argparse4j](https://github.com/argparse4j/argparse4j)
1. [Python: Using getpass with argparse](https://stackoverflow.com/a/57355741/6146580)
