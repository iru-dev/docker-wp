FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
wget \
tar


RUN wget https://wordpress.org/latest.tar.gz
RUN tar -xzvf latest.tar.gz -C /var/www
RUN mv /var/www/wordpress/* /var/www/

RUN ls -lah /var/www

VOLUME ./nginx/www /var/www
WORKDIR /var/www
CMD ["php-fpm"]
