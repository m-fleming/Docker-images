# NJOY2016 Docker images

Within these subfolders you will find Dockerfiles that define the builds for Docker images
containing compiled NJOY2016 ready for use. All of these images are in the 
`njoy21/njoy2016` repository, but there are different tags, based on the 
[NJOY2016 release versions](https://github.com/njoy/NJOY2016/releases), 
which are then interpreted by Docker:

- `21`:  This is the version NJOY2016.21 associated with the git tag `2016.21`.
- `23`:  This is the version NJOY2016.23 associated with the git tag `2016.23`.
- `24`:  This is the version NJOY2016.24 associated with the git tag `2016.24`.
- `44`:  This is the version NJOY2016.44 associated with the git tag `2016.44`.

You can find these images on the [NJOY Docker Hub](https://hub.docker.com/r/njoy21/njoy2016) 
and, with a operating version of Docker on your machine, download them using:

```
docker pull njoy21/njoy2016:44
```

where the NJOY release version is appended as the image tag (in this case version 44).
