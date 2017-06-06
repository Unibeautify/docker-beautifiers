FROM ruby:alpine

LABEL io.whalebrew.name 'ruby-beautify'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN gem install ruby-beautify

ENTRYPOINT ["ruby-beautify"]
CMD ["--help"]