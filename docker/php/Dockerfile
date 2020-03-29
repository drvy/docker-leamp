FROM

RUN apt-get update && apt-get install -y \
    curl libicu-dev libzip-dev libpng-dev zlib1g-dev libcurl4-openssl-dev

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

RUN docker-php-ext-install zip
RUN docker-php-ext-enable zip

RUN docker-php-ext-install gd
RUN docker-php-ext-enable gd

RUN docker-php-ext-install mysqli
RUN docker-php-ext-enable mysqli

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-enable pdo_mysql

RUN docker-php-ext-install curl
RUN docker-php-ext-enable curl

RUN a2enmod rewrite
