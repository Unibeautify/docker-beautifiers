FROM php:7.1-alpine@sha256:bc2f1cf36ef3c091d2fd26bae032f5b72944dd1a99bfcb2cdf4f7bd375908cb7

LABEL io.whalebrew.name 'phpcbf'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pear install PHP_CodeSniffer

ENTRYPOINT ["phpcbf"]
CMD ["--help"]