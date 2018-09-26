FROM php:5.6.36-apache
MAINTAINER Damien Retzinger <damienwebdev@gmail.com>

RUN apt-get update && apt-get install -y \
    libmcrypt-dev \
    libxslt-dev \
    libicu-dev \
    zlib1g-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev

RUN a2enmod rewrite && a2enmod headers

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd intl mcrypt pdo_mysql xsl zip opcache

ENV PHP_MEMORY_LIMIT 2G

COPY ./php.ini /usr/local/etc/php/

RUN service apache2 restart
