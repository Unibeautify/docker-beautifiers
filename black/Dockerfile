FROM python:3-alpine as black-build

# we don't want gcc in the final image, so let's do a multi stage build
RUN apk update && apk add --no-cache build-base
RUN pip install --user --upgrade black

FROM python:3-alpine

LABEL io.whalebrew.name 'black'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

# copy only the installed files from black
COPY --from=black-build /root/.local /root/.local
ENV PATH=/root/.local/bin:$PATH

ENTRYPOINT ["black"]
CMD ["--help"]