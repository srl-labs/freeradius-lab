# SR Linux authentication with FreeRADIUS

Testing radius (from radius container):

```bash
docker exec -it clab-radius-radius /bin/bash
root@radius:/# echo User-Name='alice',User-Password='alice123' | radclient -P udp 127.0.0.1:1812 auth clab-demo
Sent Access-Request Id 70 from 0.0.0.0:ed8d to 127.0.0.1:1812 length 45
Received Access-Accept Id 70 from 127.0.0.1:714 to 127.0.0.1:60813 length 33
```

Debug output is turned on for radius. See output using docker logs: `docker logs -f clab-radius-radius`
