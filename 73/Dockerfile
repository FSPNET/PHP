FROM php:7.3-fpm-alpine

RUN set -xe && \
      apk update && apk add --no-cache --virtual .build-deps \
      autoconf \
      g++ \
      libtool \
      make \
      pcre-dev \
      libxml2-dev && \
      apk add --no-cache \
      postgresql-dev \
      freetype-dev \
      libpng-dev \
      tzdata \
      unzip \
      imagemagick-dev \
      libintl \
      libzip-dev \
      icu \
      icu-dev \
      gettext-dev \
      libjpeg-turbo-dev \
      libmcrypt-dev \
      openssl && \
    docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ && \
    docker-php-ext-configure opcache --enable-opcache && \
    docker-php-ext-install gd pdo_mysql mysqli pgsql pdo_pgsql opcache zip xmlrpc exif bcmath intl zip soap iconv gettext sockets pdo mbstring && \
    pecl install redis && \
    pecl install imagick && \
    pecl install xdebug-beta && \
    docker-php-ext-enable redis imagick xdebug && \
    curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer && \
    apk del .build-deps && \
    rm -rf /var/cache/apk/ /var/lib/apk /etc/apk/cache/ 

COPY php.ini /usr/local/etc/php/php.ini

CMD ["php-fpm"]