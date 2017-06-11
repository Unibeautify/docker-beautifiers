FROM ocaml/opam

LABEL io.whalebrew.name 'ocp-indent'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN opam install --yes ocp-indent

ENTRYPOINT ["ocp-indent"]
CMD ["--help"]