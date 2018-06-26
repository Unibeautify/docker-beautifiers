FROM alpine:latest@sha256:8c03bb07a531c53ad7d0f6e7041b64d81f99c6e493cb39abba56d956b40eacbc

LABEL io.whalebrew.name 'uncrustify'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

ENV UNCRUSTIFY_VERSION 0.66.1

RUN apk upgrade --update

RUN apk add --no-cache make bash curl tar build-base cmake python3

RUN curl -fSL "https://github.com/uncrustify/uncrustify/archive/uncrustify-$UNCRUSTIFY_VERSION.tar.gz" -o uncrustify.tar.gz  \
	&& readonly NPROC=$(grep -c ^processor /proc/cpuinfo 2>/dev/null || echo 1) \
	&& echo "Using upto $NPROC threads" \
	&& mkdir -p /usr/src/uncrustify \
	&& tar -xf uncrustify.tar.gz -C /usr/src/uncrustify --strip-components=1 \
	&& rm uncrustify.tar.gz* \
	&& dir="$(mktemp -d)" \
	&& cd "$dir" \
	&& cmake /usr/src/uncrustify \
	&& make -j$NPROC \
	&& make install \
	&& rm -rf "$dir" \
	&& rm -rf /usr/src/uncrustify

ENTRYPOINT ["uncrustify"]
CMD ["--help"]