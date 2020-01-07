FROM php:7.4.1-fpm-alpine3.11

RUN set -ex \
  && apk --no-cache add \
    postgresql-dev

RUN docker-php-ext-install opcache pgsql pdo_pgsql 
