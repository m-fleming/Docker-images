FROM debian:latest

LABEL maintainer="Jeremy Lloyd Conlin jlconlin@lanl.gov"

RUN apt update \
    && apt upgrade -y \
    && apt install -y --force-yes gcc g++ gfortran clang make cmake git python3 \
    && update-alternatives --install /usr/bin/python python /usr/bin/python3 60

ENV CC /usr/bin/clang
ENV CXX /usr/bin/clang++
ENV FC /usr/bin/gfortran

ENTRYPOINT [ "/bin/bash" ]
