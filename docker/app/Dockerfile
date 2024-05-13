FROM php:8.3-fpm

WORKDIR /app

COPY ./docker/app/php.ini /usr/local/etc/php/php.ini

RUN apt-get update && apt-get install -y \
  zip \
  unzip \
  && docker-php-ext-install pdo_mysql

COPY --from=composer/composer:latest-bin /composer /usr/bin/composer
