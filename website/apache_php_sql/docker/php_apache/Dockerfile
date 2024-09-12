 
FROM php:8.2.21-apache

# # Install the PHP extensions we need
# RUN set -ex; \
# 	apt-get update; \
# 	docker-php-ext-install -j$(nproc) pdo_mysql; \
# 	rm -rf /var/lib/apt/lists/*



# RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN docker-php-ext-install mysqli 

RUN a2enmod rewrite

COPY php.ini-development /config/
RUN cp "/config/php.ini-development" "$PHP_INI_DIR/conf.d/php.ini"


