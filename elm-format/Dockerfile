FROM node:6-slim@sha256:3887fde264a6d1fd55cc4fd6943c1cd1c304f6a876d414ede35c4887ca1583a5

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