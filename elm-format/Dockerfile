FROM node:6-slim

LABEL io.whalebrew.name 'elm-format'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN npm install -g elm && \
    elm package install -y
ENV LANG=en_US.UTF-8 
RUN elm --version

RUN npm install -g elm-format@exp
RUN elm-format --help

ENTRYPOINT ["elm-format"]
CMD ["--help"]