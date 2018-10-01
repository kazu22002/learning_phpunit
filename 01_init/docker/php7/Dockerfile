FROM php:7.2.9-fpm-alpine

RUN apk add --no-cache $PHPIZE_DEPS curl \
    && pecl install xdebug \
    && docker-php-ext-install mbstring \
    && docker-php-ext-enable xdebug

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY ./php.ini /usr/local/etc/php/
COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

WORKDIR /var/www/html
