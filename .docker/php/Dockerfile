FROM php:8.2-fpm-buster

RUN apt-get update && apt-get install -y \
    git \
    unzip \
    zlib1g-dev \
    libzip-dev \
    libonig-dev

RUN docker-php-ext-install \
    pdo pdo_mysql mysqli zip exif mbstring

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html

COPY . /var/www/html