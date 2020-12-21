FROM php:7.4-fpm

RUN ls -lah
VOLUME ./nginx/www /var/www

WORKDIR /var/www

RUN apt-get update && apt-get install -y \
wget \
tar \
vim

RUN wget https://wordpress.org/latest.tar.gz &&\
tar -xzvf latest.tar.gz
#mkdir -p /var/www/blog.example.com &&\
#mv wordpress/* /var/www/blog.example.com

RUN ls -lah /var/www


CMD ["php-fpm"]
