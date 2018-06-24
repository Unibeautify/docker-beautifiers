FROM python:alpine@sha256:89d560f87a150d83a3bce87a29b3998fdb92d0836f015f16a9b3485f4dcb647f

LABEL io.whalebrew.name 'sqlformat'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pip install --upgrade sqlparse

ENTRYPOINT ["sqlformat"]
CMD ["--help"]