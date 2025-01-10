# Используем базовый образ PHP с FPM
FROM php:8.2-fpm

RUN apt-get update -y \
  && apt-get install -y \
    libonig-dev \
    libssl-dev \
    libxml2-dev \
    libz-dev \
    libzip-dev zip \
  && apt-get clean -y \ 
  && docker-php-ext-install \ 
    bcmath \
    pdo_mysql \ 
    soap \ 
    zip \
    mbstring \
    intl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]

EXPOSE 9000