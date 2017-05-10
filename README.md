# docker.sock proxy #

Exposes `/var/run/docker.sock` on `tcp://docker-sock-proxy:2375`

### Usage ###

```
docker run -v /var/run/docker.sock:/var/run/docker.sock -d --restart=always --name docker-sock-proxy docksal/socat
```

Option to allow remote connections to the host (without TLS) - **USE AT YOUR OWN RISK**

```
docker run -v /var/run/docker.sock:/var/run/docker.sock -d --restart=always --privileged -p 2375:2375 --name docker-sock-proxy docksal/socat
```
This will allow external **unsecured** connections to the Docker daemon on the host on port `2375`.
