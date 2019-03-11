FROM php:7.1-fpm

MAINTAINER Adem ARAS <adem.arass@gmail.com>

WORKDIR /var/www

# Install dependencies
RUN apt-get update \
    && apt-get install -y \
    --no-install-recommends \
    apt-utils \
    htop \
    libxml2-dev \
    libfreetype6-dev \ 
    libicu-dev \ 
    libjpeg62-turbo-dev \ 
    libmcrypt-dev \ 
    libpng-dev \ 
    libxslt1-dev \
    unzip \
    git

# Configure the gd library
RUN docker-php-ext-configure \
  	gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/;

# Install Magento Dependencies
# Install required PHP extensions
RUN docker-php-ext-install \
  	opcache \
  	bcmath \
  	gd \
  	intl \
    mysqli \
  	pdo_mysql \
  	soap \
    xml \
  	xsl \
  	zip \
    mcrypt
