FROM php:7.3-fpm

WORKDIR /var/www

RUN apt-get update && apt-get install -y \
    libzip-dev \
    libxml2-dev \
    curl \
    zip \
    unzip 

# Extension zip for laravel
RUN docker-php-ext-install \
    zip \
    bcmath \
    ctype \
    fileinfo \
    json \
    mbstring \
    pdo \
    tokenizer \
    xml \
    # extension for MySQL
    pdo_mysql \
    mysqli

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Add user for laravel application
RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

COPY . /var/www
COPY --chown=www:www . /var/www

# Change current user to www
USER www

# Expose port 9000 and start php-fpm server
EXPOSE 9000
CMD ["php-fpm"]
