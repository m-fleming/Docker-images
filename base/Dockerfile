FROM gcc:6.4.0

LABEL maintainer="Jeremy Lloyd Conlin jlconlin@lanl.gov"

RUN apt-get update && apt-get install -y python3.4 \
    # Make Python 3.4 the default Python
    && update-alternatives --install /usr/bin/python python `which python2.7` 1 \
    && update-alternatives --install /usr/bin/python python `which python3.4` 2

# Build and install CMake 3.2
RUN wget http://www.cmake.org/files/v3.2/cmake-3.2.2.tar.gz && \
    tar xf cmake-3.2.2.tar.gz && \
    cd cmake-3.2.2 && \
    ./configure && \
    make && \
    make install

ENTRYPOINT [ "/bin/bash" ]
