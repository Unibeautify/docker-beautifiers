FROM golang:alpine@sha256:56db23d665e5002b18b25be63d3bac151694438e07b29743e4d03cfa40972016

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