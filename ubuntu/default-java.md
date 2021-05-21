# Set Default Java Version

Install Java.

```bash
sudo apt install openjdk-8-jre
sudo apt install openjdk-11-jre
```

Set the default version.

```bash
sudo update-alternatives --set java /usr/lib/jvm/java-11-openjdk-amd64/bin/java
```

List the alternatives.

```bash
update-alternatives --list java
/usr/lib/jvm/java-11-openjdk-amd64/bin/java
/usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java
```

Confirm.

```bash
which java
/usr/bin/java
java -version
openjdk version "11.0.11" 2021-04-20
OpenJDK Runtime Environment (build 11.0.11+9-Ubuntu-0ubuntu2.20.04)
OpenJDK 64-Bit Server VM (build 11.0.11+9-Ubuntu-0ubuntu2.20.04, mixed mode, sharing)
```

To configure the Java runtime interactively, use the `--config` switch.

```bash
update-alternatives --config java
There are 2 choices for the alternative java (providing /usr/bin/java).

  Selection    Path                                            Priority   Status
------------------------------------------------------------
  0            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1111      auto mode
* 1            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1111      manual mode
  2            /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java   1081      manual mode

Press <enter> to keep the current choice[*], or type selection number:
```

## References

1. [How to Install OpenJDK 11 in Ubuntu 18.04](https://www.ubuntu18.com/ubuntu-install-openjdk-11/)
1. [How to use the command update-alternatives --config java](https://stackoverflow.com/questions/12787757/how-to-use-the-command-update-alternatives-config-java)
1. [OpenJDK 8 Download and Installation on Ubuntu](https://techoral.com/blog/java/install-openjdk-8-ubuntu.html)
