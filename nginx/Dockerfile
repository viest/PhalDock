FROM nginx:alpine

MAINTAINER VikinDev "vikindev@outlook.com"

ADD nginx.conf /etc/nginx/
COPY default/*.conf /etc/nginx/sites-available/

ARG PHP_UPSTREAM=php-fpm

RUN apk update && \
    apk upgrade && \
    apk add --no-cache bash && \
    adduser -D -H -u 1000 -s /bin/bash www-data && \
    rm /etc/nginx/conf.d/default.conf && \
    echo "upstream php-upstream { server ${PHP_UPSTREAM}:9000; }" > /etc/nginx/conf.d/upstream.conf

CMD ["nginx"]

EXPOSE 80 443