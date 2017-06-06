FROM debian:sid-slim

RUN apt-get update && \
    apt-get install -y clang-format-5.0

# switch to uid/gid identical to host uid/gid (forks/users), if not doing this, files that
# clang-format written will change user and group all to root.
USER 1000:100

ENTRYPOINT ["clang-format-5.0"]
CMD ["--help"]