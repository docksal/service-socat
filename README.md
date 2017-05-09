# Socat Docker image for Docksal #

This is a socat image which proxies tcp://socat:2375 to /var/run/docker.sock

### Usage ###

* Build: `fin docker build -t docksal-socat:latest .`
* Run: `fin docker run -v /var/run/docker.sock:/var/run/docker.sock -d --restart=always --name docksal-socat  docksal-socat`
* Option to allow remote petitions to the host (without TLS):
  Run: `docker run --privileged -v /var/run/docker.sock:/var/run/docker.sock -p 2375:2375 -d --restart=always --name docksal-socat docksal-socat`

