FROM ruby:alpine as builder

RUN apk update \
    && apk add --virtual build-dependencies \
        build-base \
    && true

RUN gem install rubocop -v 0.64.0
RUN gem install rubocop-rspec -v 1.32.0

RUN rm -rf /usr/local/bundle/cache/*.gem \
 && find /usr/local/bundle/gems/ -name "*.c" -delete \
 && find /usr/local/bundle/gems/ -name "*.o" -delete

FROM ruby:alpine

LABEL io.whalebrew.name 'rubocop'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

COPY --from=builder /usr/local/ /usr/local/

ENTRYPOINT ["rubocop"]
CMD ["--help"]
