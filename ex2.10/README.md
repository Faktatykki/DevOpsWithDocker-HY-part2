Instructions in docker-compose file comments

nginx.conf file included even though not explicitly asked

When running: 

```
docker run -it --rm --network host networkstatic/nmap localhost
```

Original report said (some censoring included, since some other ports were open too):


Starting Nmap 7.92 ( https://nmap.org ) at 2023-05-10 16:32 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0000040s latency).
Not shown: 994 closed tcp ports (reset)
PORT     STATE SERVICE
---/tcp  open  ---
80/tcp   open  http
111/tcp  open  rpcbind
---/tcp  open  ---
5000/tcp open  upnp
8080/tcp open  http-proxy

Nmap done: 1 IP address (1 host up) scanned in 0.17 seconds

After fixes:

Starting Nmap 7.92 ( https://nmap.org ) at 2023-05-10 17:04 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0000040s latency).
Not shown: 996 closed tcp ports (reset)
PORT    STATE SERVICE
---/tcp open  ---
80/tcp  open  http
111/tcp open  rpcbind
---/tcp open  ---
