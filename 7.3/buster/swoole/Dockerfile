FROM knik/php:7.3-cli-buster

RUN pecl bundle --destination=/usr/src/php/ext swoole \
	&& docker-php-ext-install swoole
