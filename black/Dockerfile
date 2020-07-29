FROM python:3-alpine

LABEL io.whalebrew.name 'black'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

# we don't want gcc in the final image, so remove it in one docker layer
RUN apk add --no-cache build-base \
    && pip install --no-cache-dir --upgrade black \
    && apk del build-base

ENTRYPOINT ["black"]
CMD ["--help"]