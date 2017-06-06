FROM python:alpine

LABEL io.whalebrew.name 'beautysh'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN pip install --upgrade beautysh

ENTRYPOINT ["beautysh"]
CMD ["--help"]