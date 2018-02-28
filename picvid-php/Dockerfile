FROM php:7.2-fpm

RUN apt-get update
RUN docker-php-ext-install -j$(nproc) pdo_mysql
RUN docker-php-ext-install -j$(nproc) exif