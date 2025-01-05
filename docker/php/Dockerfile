FROM php:7-fpm

# Install system dependencies
RUN apt-get update && apt-get install -y procps zip unzip libzip-dev libpq-dev vim git unzip \
  && pecl install \
  apcu \
  xdebug-3.1.0 \
  redis \
  && docker-php-ext-enable \
  apcu \
  xdebug \
  redis 

# Install PHP extensions Type docker-php-ext-install to see available extensions
RUN docker-php-ext-install pdo pdo_mysql pdo_pgsql mysqli zip

# Get latest Composer
COPY --from=composer:2.7.2 /usr/bin/composer /usr/bin/composer 

# Enable PHP XDebug Extension
COPY ./xdebug.ini /tmp/xdebug.ini
RUN cat /tmp/xdebug.ini >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN rm /tmp/xdebug.ini

WORKDIR /var/www
