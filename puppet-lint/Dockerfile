FROM ruby:alpine@sha256:15e425d2b978927772ec0657050cd3052e2b5d444dc599794e145ad0b9b01cda

LABEL io.whalebrew.name 'puppet-lint'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN gem install puppet-lint

ENTRYPOINT ["puppet-lint"]
CMD ["--help"]