FROM php:7.3-alpine

LABEL io.whalebrew.name 'phpcbf'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pear install PHP_CodeSniffer

ENTRYPOINT ["phpcbf"]
CMD ["--help"]