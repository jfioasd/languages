#syntax=docker/dockerfile-upstream:1.4.0-rc1
FROM attemptthisonline/base

# THE_ prefix because $BASH_VERSION is a special variable
ARG THE_BASH_VERSION=5.1.16

RUN curl -L https://ftpmirror.gnu.org/bash/bash-$THE_BASH_VERSION.tar.gz | \
    tar -xz && \
    cd bash-$THE_BASH_VERSION && \
    ./configure && \
    make -j $(nproc) && \
    make install && \
    cd / && \
    rm -rf /tmp/bash-$THE_BASH_VERSION
