FROM credit-php:5.6-apache

RUN pecl install xdebug

COPY php.ini /usr/local/etc/php/conf.d/dev.ini

RUN install --mode=0644 --owner=www-data --group=www-data /dev/null /var/log/xdebug.log