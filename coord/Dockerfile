FROM        fedora:22
MAINTAINER  numayacto@gmail.com

RUN dnf update -y
RUN dnf install wget gcc gcc-c++ autoconf git -y
RUN mkdir -p /sources
RUN mkdir -p /pkgbatch
COPY ./pkgbatch /
RUN ln -s /pkgbatch/pkgbatch /usr/bin/pkgbatch

COPY HyperDexSources/hyperdex.sources /sources/hyperdex.sources
RUN cat /sources/hyperdex.sources | pkgbatch install -e

EXPOSE 1982

RUN mkdir -p /hyperdex/coord
VOLUME /hyperdex
