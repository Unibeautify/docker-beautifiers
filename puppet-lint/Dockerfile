FROM ruby:alpine

LABEL io.whalebrew.name 'puppet-lint'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN gem install puppet-lint

ENTRYPOINT ["puppet-lint"]
CMD ["--help"]