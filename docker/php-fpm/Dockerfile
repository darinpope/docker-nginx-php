FROM php:5.6.38-fpm-stretch

ENV TZ=America/New_York

COPY ./conf/downtowner.ini /usr/local/etc/php/conf.d/downtowner.ini

RUN echo $TZ > /etc/timezone \
    && dpkg-reconfigure -f noninteractive tzdata \
    && apt-get update \
    && apt-get install -y libmcrypt-dev libpng-dev \
    && docker-php-ext-install mcrypt \
    && docker-php-ext-install gd 
    
CMD ["php-fpm"]

EXPOSE 9000