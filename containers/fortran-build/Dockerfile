FROM gcc:latest
LABEL authors="Alexandre Mechineau"

ENV DEBIAN_FRONTEND=noninteractive

RUN set -ex ; \
    apt-get update ; \
    apt-get install -y --no-install-recommends \
        locales pkg-config \
        python3-pip git \
        cmake ninja-build \
        lcov valgrind \
        doxygen ; \
    rm -rf /var/lib/apt/lists/* ; \
    localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8

# Make sure we have a proper unicode locale and language
ENV LANG en_US.utf8
