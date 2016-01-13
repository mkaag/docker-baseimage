docker-base-image
=================

[![Docker Hub](https://img.shields.io/badge/docker-mkaag%2Fbaseimage-008bb8.svg)](https://registry.hub.docker.com/u/mkaag/baseimage/)
[![](https://badge.imagelayers.io/mkaag/baseimage:latest.svg)](https://imagelayers.io/?images=mkaag/baseimage:latest 'Get your own badge on imagelayers.io')

This repository contains the **Dockerfile** and the configuration files to build a base image for [Docker](https://www.docker.com/).

### Base Docker Image

* [phusion/baseimage](https://github.com/phusion/baseimage-docker), the *minimal Ubuntu base image modified for Docker-friendliness*...
* ...[including image's enhancement](https://github.com/racker/docker-ubuntu-with-updates) from [Paul Querna](https://journal.paul.querna.org/articles/2013/10/15/docker-ubuntu-on-rackspace/)

### Installation

```bash
docker build -t mkaag/baseimage github.com/mkaag/docker-baseimage
```

### Usage

#### Basic usage

```bash
docker run -ti --rm mkaag/baseimage /sbin/my_init -- bash -l
```

### Using as base image
```
FROM mkaag/baseimage:latest

# Use baseimage-docker's init system.
CMD ["/sbin/my_init"]

# ...put your own build instructions here...

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```
