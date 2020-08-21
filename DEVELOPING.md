# Developing

## Building the image

### Base OS image

```bash
$ NDNSIM_DOCKER_OS_VERSION=20.04
$ cd base-${NDNSIM_DOCKER_OS_VERSION}
$ docker build --no-cache --tag localndnsimbase:${NDNSIM_DOCKER_OS_VERSION} .
```

### ndnSIM image

See [fam4r/docker-ndnsim](https://github.com/fam4r/docker-ndnsim/blob/master/DEVELOPING.md#ndnsim-image).
