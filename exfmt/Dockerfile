FROM elixir

LABEL io.whalebrew.name 'exfmt'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN mix help exfmt

ENTRYPOINT ["mix", "exfmt"]
