FROM python:alpine

LABEL io.whalebrew.name 'autopep8'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pip install --upgrade autopep8

ENTRYPOINT ["autopep8"]
CMD ["--help"]