FROM njoy21/njoy:base

LABEL maintainer="Jeremy Lloyd Conlin jlconlin@lanl.gov"

RUN apt-get update \
    && update-alternatives --install /usr/bin/python python `which python2.7` 3 \
    && apt-get install software-properties-common -y \
    && update-alternatives --install /usr/bin/python python `which python3.4` 4 \
    && add-apt-repository 'deb http://apt.llvm.org/precise llvm-toolchain-precise-3.8 main' \
    && apt-get update  \
    && apt-get install -y --force-yes clang-3.8 \
    && update-alternatives --install /usr/bin/clang clang `which clang-3.8` 1 \
                           --slave /usr/bin/clang++ clang++ `which clang++-3.8` \
    && update-alternatives --install /usr/local/bin/cc cc `which clang` 100 \
    && update-alternatives --install /usr/local/bin/c++ c++ `which clang++` 100 \
    && echo

ENTRYPOINT [ "/bin/bash" ]
