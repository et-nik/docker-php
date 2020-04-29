FROM php:7.4-fpm-alpine

ENV TZ=Europe/Moscow

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone \
    && apk update && apk add --update-cache \
        libmcrypt-dev \
        libc-dev \
        freetype \
        freetype-dev \
        libjpeg-turbo-dev \
        libpng-dev \
        libxpm-dev \
        icu-dev  \
        libxslt-dev \
        libmemcached-dev \
        bzip2 \
        bzip2-dev \
        libzip-dev \
        libxml2-dev \
        gmp-dev \
        gettext-dev \
    && rm -rf /var/cache/apk/*

RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install \
        bcmath \
        bz2 \
        calendar \
        dba \
        exif \
        gd \
        gettext \
        mysqli \
        pcntl \
        pdo_mysql \
        shmop \
        soap \
        sockets \
        sysvmsg \
        sysvsem \
        sysvshm \
        zip \
        opcache \
        gmp \
        intl \
    && rm -rf /usr/src/php/*
