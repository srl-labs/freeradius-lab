# SR Linux authentication with FreeRADIUS

Testing radius (from radius container):

```bash
docker exec -it clab-radius-radius /bin/bash
root@radius:/# echo User-Name='alice',User-Password='alice123' | radclient -4 -c 1 -r 2 -t 4 -P udp 127.0.0.1:1812 auth clab-demo
Sent Access-Request Id 87 from 0.0.0.0:edf2 to 127.0.0.1:1812 length 45
Received Access-Accept Id 87 from 127.0.0.1:714 to 127.0.0.1:60914 length 33
```
