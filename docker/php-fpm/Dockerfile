FROM php:5.6.38-fpm-stretch

RUN apt-get update \
    && apt-get install -y libmcrypt-dev libpng-dev \
    && docker-php-ext-install mcrypt \
    && docker-php-ext-install gd 
    
CMD ["php-fpm"]

EXPOSE 9000