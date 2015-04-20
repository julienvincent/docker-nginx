## Nginx Dockerfile

This repository contains **Dockerfile** of [nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/julienvincent/nginx/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [julienvincent/ubuntu](https://registry.hub.docker.com/u/julienvincent/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/julienvincent/nginx/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull julienvincent/nginx`

   (alternatively, you can build an image from the Dockerfile: `docker build -t="julienvincent/nginx" github.com/julienvincent/nginx`)


### Usage

    docker run -d -p 80:80 julienvincent/nginx

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/sites-enabled -v <certs-dir>:/etc/nginx/certs julienvincent/nginx

After few seconds, open `http://<host>` to see the welcome page.
