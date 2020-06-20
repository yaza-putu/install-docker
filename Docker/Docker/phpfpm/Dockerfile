FROM php:7.2-fpm

RUN apt-get update && apt-get install -y \
        curl \
        wget \
        git \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpq-dev \
        libzip-dev  \
        libicu-dev  \
        && docker-php-ext-install -j$(nproc) iconv mbstring mysqli pdo_mysql zip pdo_pgsql pgsql \
        && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
        && docker-php-ext-install gd
