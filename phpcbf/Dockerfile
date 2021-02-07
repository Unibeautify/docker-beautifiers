FROM php:7.4-alpine

LABEL io.whalebrew.name 'phpcbf'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pear install PHP_CodeSniffer

ENTRYPOINT ["phpcbf"]
CMD ["--help"]