FROM njoy21/njoy:llvm

LABEL maintainer="Jeremy Lloyd Conlin jlconlin@lanl.gov"

RUN cd ~ \
    && git clone https://github.com/njoy/NJOY2016.git \
    && cd NJOY2016 \
    && git checkout tags/21 -b 2016.21 \
    && mkdir bin \
    && cd bin \
    && export CORES=$(grep -c ^processor /proc/cpuinfo) \
    && cmake -D CMAKE_BUILD_TYPE=Release \
             -D static_libraries=TRUE \
             ../ \
    && make -j${CORES} \
    && make install 

