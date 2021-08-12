FROM php:7.4-fpm

COPY php/php.ini /usr/local/etc/php/

RUN docker-php-ext-install pdo pdo_mysql mysqli \
    && pecl install xdebug && docker-php-ext-enable xdebug

RUN apt-get update && apt-get install -y \
    imagemagick libmagickwand-dev --no-install-recommends \
    libzip-dev \
    zip \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    && pecl install imagick \
    && docker-php-ext-enable imagick \
    && docker-php-ext-install zip \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd