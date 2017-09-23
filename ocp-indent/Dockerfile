FROM ocaml/opam

SHELL ["/bin/sh", "-lc"]
LABEL io.whalebrew.name 'ocp-indent'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN opam init --auto-setup
RUN opam install --yes ocp-indent
RUN ocp-indent --help

ENTRYPOINT ["ocp-indent"]
CMD ["--help"]