FROM php:7.2.3-alpine@sha256:2484481d88b3ab30a75cd4940bb89684aa883b61fd616fd859de2d9d87c103b8

LABEL io.whalebrew.name 'php-cs-fixer'
LABEL io.whalebrew.config.working_dir '/project'
WORKDIR /project

RUN wget https://github.com/FriendsOfPHP/PHP-CS-Fixer/releases/download/v2.11.1/php-cs-fixer.phar -O php-cs-fixer \
  && chmod a+x php-cs-fixer \
  && mv php-cs-fixer /usr/local/bin/php-cs-fixer

ENTRYPOINT ["php-cs-fixer"]
CMD ["--help"]