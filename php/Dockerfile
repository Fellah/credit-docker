FROM php:5-apache

## Set custom configs for Apache
COPY apache2.conf /etc/apache2/conf-available/credit.conf
RUN ln -s /etc/apache2/conf-available/credit.conf /etc/apache2/conf-enabled

## Set custom PHP.INI for project
COPY php.ini /usr/local/etc/php/php.ini

#RUN apt-get update -y
#RUN apt-get install -y imagemagick
