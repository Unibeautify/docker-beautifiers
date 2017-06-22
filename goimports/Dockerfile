FROM golang:alpine

LABEL io.whalebrew.name 'goimports'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN apk add --no-cache --virtual .build-deps \
		git \
        ; \
        go get golang.org/x/tools/cmd/goimports && \
        rm -rf /go/src/golang.org \
        apk del .build-deps;

ENTRYPOINT ["goimports"]
CMD ["--help"]