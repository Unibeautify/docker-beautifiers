FROM php:7.3.6-alpine

LABEL io.whalebrew.name 'php-cs-fixer'
LABEL io.whalebrew.config.working_dir '/project'
WORKDIR /project

RUN wget https://github.com/FriendsOfPHP/PHP-CS-Fixer/releases/download/v2.14.2/php-cs-fixer.phar -O php-cs-fixer \
  && chmod a+x php-cs-fixer \
  && mv php-cs-fixer /usr/local/bin/php-cs-fixer

ENTRYPOINT ["php-cs-fixer"]
CMD ["--help"]
