FROM php:php7-fpm
RUN apt-get update && apt-get upgrade \
    apt-get install -y \
    && docker-php-ext-install -j$(nproc) iconv mcrypt \
