## samples

- use it like http client

    printf "GET / HTTP/1.0\nHOST: www.bing.com" | nc www.bing.com 80

- open port scanning

    nc -znv[v] -w 5 192.168.0.1 1-1000

- tcp[or udp] server

    nc -l[u] -p 3333

- tcp[or udp] client

    nc [-u] SERVER_IP 3333

- pipe via UDP (-u) with a wait time (-w) of 1 second to "loggerhost" on port 514

    echo '<0>message' | nc -w 1 -u loggerhost 514

- proxy and port forwarding:

    nc -l port | nc hostname port

- serve a file

    nc -l PORT < FILE

- receive a file:

    nc www.bing.com 80 > FILE

- server stay up after client detach:

    nc -k -l port

- client stay up after EOF:

    nc -q timeout ip_address

- making any process a server

    nc -l -p 1234 -e /bin/sh

## references:

- https://en.wikipedia.org/wiki/Netcat
- https://github.com/tldr-pages/tldr
