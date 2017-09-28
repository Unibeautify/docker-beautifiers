FROM ocaml/opam

SHELL ["/bin/bash", "-lc"]
LABEL io.whalebrew.name 'ocp-indent'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN opam install --yes ocp-indent
RUN ocp-indent --help

COPY docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["--help"]
