#
# Nginx Dockerfile
#
# https://github.com/dockerfile/nginx
#

# Pull base image.
FROM nginx:1.7.10

RUN \
    apt-get update && \
    apt-get -y install supervisor && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir -p /data/www

COPY container/nginx.conf /etc/nginx/nginx.conf
COPY container/default.conf /etc/nginx/conf.d/default.conf
COPY container/index.html /data/www/index.html

# Define mountable directories.
VOLUME ["/etc/nginx/conf.d", "/data/www"]

# Define default command
CMD ["nginx"]

# Expose ports.
EXPOSE 80 443