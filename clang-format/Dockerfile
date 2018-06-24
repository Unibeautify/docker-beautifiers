FROM debian:sid-slim@sha256:8a8026a8ecb84144928e70ec33be07eb17e59d165ed45f31ebd4081296d2a543

RUN apt-get update && \
    apt-get install -y clang-format-6.0

# switch to uid/gid identical to host uid/gid (forks/users), if not doing this, files that
# clang-format written will change user and group all to root.
USER 1000:100

ENTRYPOINT ["clang-format-6.0"]
CMD ["--help"]