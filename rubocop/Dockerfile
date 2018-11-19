FROM ruby:alpine

LABEL io.whalebrew.name 'rubocop'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN apk add --update make g++
RUN gem install rubocop

ENTRYPOINT ["rubocop"]
CMD ["--help"]
