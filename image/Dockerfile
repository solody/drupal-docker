FROM drupal:latest

RUN apt-get update && apt-get install -y \
            wget \
             && docker-php-ext-install -j$(nproc) bcmath

COPY install-composer.sh install-composer.sh

RUN chmod 0777 "./install-composer.sh"
RUN "./install-composer.sh"


RUN php composer.phar update

COPY composer.json composer.json