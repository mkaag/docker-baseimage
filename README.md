docker-base-image
=================

[![Docker Hub](https://img.shields.io/badge/docker-mkaag%baseimage-008bb8.svg)](https://registry.hub.docker.com/u/mkaag/baseimage/)

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
docker run -d mkaag/baseimage
```

```
FROM mkaag/baseimage:latest
...
```