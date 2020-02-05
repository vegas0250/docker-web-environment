FROM php:7.4.1-cli-alpine3.11

RUN set -ex \
  && apk --no-cache add \
    postgresql-dev zlib-dev 

RUN apk --no-cache update \
    && apk --no-cache upgrade \
    && apk add --no-cache $PHPIZE_DEPS \
        freetype \
        freetype-dev \
        libjpeg-turbo \
        libjpeg-turbo-dev \
        libpng \
        libpng-dev

RUN docker-php-ext-configure gd --with-freetype --with-jpeg

RUN docker-php-ext-install pgsql pdo_pgsql gd
