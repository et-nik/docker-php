FROM knik/php:8.0-cli-alpine

RUN pecl bundle --destination=/usr/src/php/ext swoole \
	&& docker-php-ext-install swoole \
	&& rm -rf /usr/src/php/*
