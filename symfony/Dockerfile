FROM php:7.4-cli-alpine

RUN apk update \
  && apk add \
  git \
  curl \
  wget \
  bash

RUN mkdir -p /usr/local/bin \
  && wget https://get.symfony.com/cli/installer -O - | bash \
  && ln -s /root/.symfony/bin/symfony /usr/local/bin/symfony

RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/local/bin --filename=composer

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN set -xe \
    && apk add --no-cache --update --virtual .phpize-deps $PHPIZE_DEPS

WORKDIR /app

EXPOSE 9000

CMD symfony server:start --port 9000 --no-tls