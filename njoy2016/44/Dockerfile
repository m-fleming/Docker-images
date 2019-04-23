FROM njoy21/njoy:llvm

MAINTAINER LANL <Jeremy Lloyd Conlin jlconlin@lanl.gov>

LABEL org.label-schema.description="Docker image for NJOY2016" \
      org.label-schema.url="https://www.njoy21.io/NJOY2016/" \
      org.label-schema.vcs-url="https://github.com/njoy/Docker-images/"

RUN cd ~ \
    && git clone https://github.com/njoy/NJOY2016.git \
    && cd NJOY2016 \
    && git checkout tags/2016.44 -b 2016.44 \
    && mkdir bin \
    && cd bin \
    && export CORES=$(grep -c ^processor /proc/cpuinfo) \
    && cmake -D CMAKE_BUILD_TYPE=Release \
             -D static_libraries=TRUE \
             ../ \
    && make -j${CORES} \
    && make install 

