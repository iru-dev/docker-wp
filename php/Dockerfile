FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
wget \
tar \
vim


RUN wget https://wordpress.org/latest.tar.gz;
RUN tar -xzvf latest.tar.gz;
RUN mkdir -p /var/www/blog.example.com
RUN mv wordpress/* /var/www/blog.example.com

RUN ls -lah /var/www/blog.example.com

#VOLUME ./nginx/www /var/www
WORKDIR /var/www

CMD ["php-fpm"]
