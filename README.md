# Nginx Dockerfile

This repository contains an automated **Dockerfile** of [nginx](http://nginx.org/)

## Supported tags

+ `latest`
+ `1.9.2`
+ `1.7.10`

### Base Docker Image

* [nginx](https://registry.hub.docker.com/u/library/nginx/)

### Usage

    docker run --name nginx -v /some/content:/data/www -d julienvincent/nginx