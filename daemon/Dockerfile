FROM        fedora:22
MAINTAINER  numayacto@gmail.com

RUN dnf update -y
RUN dnf install wget gcc gcc-c++ autoconf pkgconfig git
RUN git clone https://github.com/NuMayaLLC/pkgbatch.git
RUN git clone https://github.com/NuMayaLLC/HyperDexSources.git
RUN cat ./HyperDexSources/hyperdex.sources | ./pkgbatch/pkgbatch install

EXPOSE 1982

RUN mkdir -p /hyperdex/daemon
VOLUME /hyperdex

