FROM php:8.2-alpine

LABEL maintainer="florian@go2tech.de"

COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer

RUN apk add --no-cache --no-progress libpng-dev tar icu-dev jq git linux-headers

RUN docker-php-ext-install gd pcntl pdo_mysql mysqli intl sockets calendar
