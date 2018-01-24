# NJOY Docker images
Here are the Dockerfiles that create the base Docker images used in NJOY development and testing. All of these are in the `njoy21/njoy` repository, but there are different "tags"

- `base`: 
  This is the `njoy21/njoy:base` Docker image. As it's name indicates, it is the base for every other image. Here we have the following installed:
  - gcc 6.4.0
  - Python 3.4
  - CMake 3.2

- `llvm`:
  This is the `njoy21/njoy:llvm` Docker image and is based on `njoy21/njoy:base`. This images adds the following:
  - llvm 3.8
