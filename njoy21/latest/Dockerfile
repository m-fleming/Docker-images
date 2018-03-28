FROM njoy21/njoy:base

LABEL maintainer="Jeremy Lloyd Conlin jlconlin@lanl.gov"

# RUN /usr/bin/clang --version \
#     && /usr/bin/clang++ --version \
#     && /usr/bin/gfortran --version 

# RUN /usr/bin/clang -v \
#     && /usr/bin/clang++ -v \
#     && /usr/bin/gfortran -v 

RUN cd ~ \
    && git clone https://github.com/njoy/NJOY21.git \
    && cd NJOY21 \
    && git checkout bugfix/POWR-Lib3-test \
    && mkdir bin \
    && cd bin \
    && export CORES=$(grep -c ^processor /proc/cpuinfo) \
    && cmake -D CMAKE_BUILD_TYPE=Release \
             -D static_libraries=TRUE \
             ../ \
    && make -j${nproc} \
    && make install 

ENTRYPOINT [ "/bin/bash" ]
