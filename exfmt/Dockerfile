FROM elixir

LABEL io.whalebrew.name 'exfmt'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN mix local.hex --force
RUN mix archive.install github lpil/exfmt --force

RUN mix help exfmt

ENTRYPOINT ["mix", "exfmt"]
