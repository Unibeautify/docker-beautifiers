FROM ruby:alpine

LABEL io.whalebrew.name 'sass-convert'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN gem install sass

ENTRYPOINT ["sass-convert"]
CMD ["--help"]