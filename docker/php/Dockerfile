FROM php:7.4-fpm

RUN apt update && apt install -y vim git curl wget zip unzip postgresql-client libpq-dev

RUN apt clean && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install pgsql pdo_pgsql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 9000

CMD ["php-fpm"]
