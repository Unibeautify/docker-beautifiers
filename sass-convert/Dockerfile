FROM ruby:alpine@sha256:15e425d2b978927772ec0657050cd3052e2b5d444dc599794e145ad0b9b01cda

LABEL io.whalebrew.name 'sass-convert'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN apk add --update build-base libffi-dev
RUN gem install sass

ENTRYPOINT ["sass-convert"]
CMD ["--help"]