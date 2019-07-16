FROM php:7.2-apache-stretch
MAINTAINER Damien Retzinger <damienwebdev@gmail.com>

RUN apt-get update && apt-get install -y \
    libxslt-dev \
    libicu-dev \
    zlib1g-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd intl pdo_mysql xsl zip opcache

COPY ./php.ini /usr/local/etc/php/

RUN a2enmod rewrite && a2enmod headers && service apache2 restart
