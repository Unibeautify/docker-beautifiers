FROM python:alpine

LABEL io.whalebrew.name 'sqlformat'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pip install --upgrade sqlparse

ENTRYPOINT ["sqlformat"]
CMD ["--help"]