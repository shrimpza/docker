**To build the image:**

```
$ docker build -t you/sflowtrend .
```

**To create the container:**

```
docker run --name=sflowtrend -p 8087:8087 -p 6343:6343/udp -v /var/local/sflowtrend-pro:/var/local/sflowtrend-pro you/sflowtrend
```

Makes port 8087 (TCP, web front-end) and 6343 (UDP, sFlow server port) available via the host, and maps storage from the host in `/var/local/sflowtrend-pro`.

**To start it later:**

```
docker start sflowtrend
```
