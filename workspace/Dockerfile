FROM ubuntu:14.04

RUN sed -i 's/http:\/\/archive\.ubuntu\.com\/ubuntu\//http:\/\/mirrors\.aliyun\.com\/ubuntu\//g' /etc/apt/sources.list

RUN echo 'deb http://ppa.launchpad.net/ondrej/php/ubuntu trusty main' > /etc/apt/sources.list.d/php.list

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E5267A6C

RUN apt-get update && \
       apt-get install -y php7.0-cli \
       php7.0-curl \
       php7.0-mcrypt \
       php7.0-mysql \
       php7.0-gd \
       php7.0-xml \
       php7.0-dev \
       php7.0-zip \
       php7.0-xml \
       php7.0-opcache \
       php7.0-mbstring \
       php7.0-intl \
       php7.0-json \
       php7.0-pgsql \
       php7.0-imap \
       php-pear \
       libsasl2-dev \
       curl \
       git

RUN mkdir -p /usr/local/openssl/include/openssl/ && \
    ln -s /usr/include/openssl/evp.h /usr/local/openssl/include/openssl/evp.h && \
    mkdir -p /usr/local/openssl/lib/ && \
    ln -s /usr/lib/x86_64-linux-gnu/libssl.a /usr/local/openssl/lib/libssl.a && \
    ln -s /usr/lib/x86_64-linux-gnu/libssl.so /usr/local/openssl/lib/

RUN curl -sS https://getcomposer.org/installer | php && \
    chmod +x composer.phar && mv composer.phar /usr/local/bin/composer

RUN useradd -m -s /bin/bash docker

WORKDIR /var/www

ADD application/* /var/www
RUN chown -R docker:docker /var/www