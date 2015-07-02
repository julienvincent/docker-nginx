# julienvincent/nginx:1.9.2

FROM nginx:1.9.2
MAINTAINER Julien Vincent "julienlucvincent@gmail.com"

RUN mkdir -p /data/www

# Install supervisor and clean
RUN apt-get -y update && \
    apt-get -y install supervisor && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Copy config
COPY container/nginx.conf /etc/nginx/nginx.conf
COPY container/default.conf /etc/nginx/conf.d/default.conf

VOLUME ["/etc/nginx/conf.d", "/data/www"]

CMD ["nginx"]
EXPOSE 80 443