FROM drupal:latest

RUN apt-get update && docker-php-ext-install -j$(nproc) bcmath

COPY install-composer.sh install-composer.sh
RUN install-composer.sh

COPY composer.json composer.json