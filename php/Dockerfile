FROM php:7.4-fpm

RUN apt-get update \
    && apt-get install -y gnupg git curl zip unzip \
    && apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 7638D0442B90D010 AA8E81B4331F7F50 9D6D8F6BC857C906 \
    && apt-get install -y libgmp-dev \
    && docker-php-ext-install gmp mysqli pdo pdo_mysql \
    && docker-php-ext-enable pdo_mysql

WORKDIR /var/www