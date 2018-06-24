FROM python:3-alpine

LABEL io.whalebrew.name 'black'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pip install --upgrade black

ENTRYPOINT ["black"]
CMD ["--help"]