FROM ruby:alpine

RUN apk update \
    && apk add --virtual build-dependencies \
        build-base \
    && true

LABEL io.whalebrew.name 'rubocop'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN gem install rubocop -v 0.64.0
RUN gem install rubocop-rspec -v 1.32.0

ENTRYPOINT ["rubocop"]
CMD ["--help"]
