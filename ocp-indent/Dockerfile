FROM ocaml/opam:latest@sha256:43152bc294d3264d63573c48972e30d9352a4472a66ec1f8e64cfb5be50b2d12

SHELL ["/bin/bash", "-lc"]
LABEL io.whalebrew.name 'ocp-indent'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN opam install --yes ocp-indent
RUN ocp-indent --help

COPY docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["--help"]
