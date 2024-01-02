# TCP Command-Line Tool

After becoming aware of the [\<BASH stack />](https://github.com/cgsdev0/bash-stack/tree/main) I also learned about [tcpserver](https://cr.yp.to/ucspi-tcp/tcpserver.html), which is a command-line tool for TCP client and server programs.

I have used [Netcat](https://nc110.sourceforge.io/) and [Ncat](https://nmap.org/ncat/) but was unaware of `tcpserver`. 😲

In the case of `bash-stack` `tcpserver` is used to invoke the core script.

```bash
PORT=${PORT:-3000}
echo -n "Listening on port "
tcpserver -1 -o -l 0 -H -R -c 1000 0 $PORT ./core.sh
```

Install `tcpserver` using `apt`.

```bash
sudo apt install ucspi-tcp
```

In terms of classification, I chose `Linux` over `Bash` since I used a Linux package manager to obtain `tcpserver`.

## References

1. [The tcpserver program](https://cr.yp.to/ucspi-tcp/tcpserver.html)
2. [Netcat](https://nc110.sourceforge.io/)
3. [Ncat](https://nmap.org/ncat/)
