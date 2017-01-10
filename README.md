# Socat Docker image for Docksal #

This is a socat image which proxies tcp://socat:2375 to /var/run/docker.sock

### Usage ###

* Build: `fin docker build -t docksal-socat:latest .`
* Run: `fin docker run -v /var/run/docker.sock:/var/run/docker.sock -d --restart=always --name docksal-socat  docksal-socat`
