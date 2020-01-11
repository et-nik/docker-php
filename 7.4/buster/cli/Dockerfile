FROM php:7.4-cli-buster

RUN apt-get -y update && apt-get -y install \
        libmcrypt-dev \
        libc-dev \
        libfreetype6 \
        libfreetype6-dev \
        libjpeg-dev \
        libjpeg62-turbo-dev \
        libxpm-dev \
        libpng-dev \
        libicu-dev  \
        libxslt-dev \
        libmemcached-dev \
        bzip2 \
        libbz2-dev \
        libzip-dev \
        libxml2-dev \
        libgmp-dev \
    --no-install-recommends && rm -r /var/lib/apt/lists/*

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
        wddx \
        zip \
        opcache \
        gmp \
        intl

RUN echo "date.timezone = Europe/Moscow" > /usr/local/etc/php/php.ini
