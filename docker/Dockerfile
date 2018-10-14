FROM php:7.2.10-apache

MAINTAINER WDD Pace

COPY . /var/www/html
COPY .docker/vhosts.conf /etc/apache2/sites-available/000-default.conf

RUN docker-php-ext-install mbstring pdo pdo_mysql \
    && a2enmod rewrite \
    && apt-get update && apt-get install -y \
    sqlite3 \
    vim-tiny

