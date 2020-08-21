# Developing

## Building the image

### Base OS image

```bash
$ NDNSIM_DOCKER_OS_VERSION=ubuntu-20.04
$ cd ${NDNSIM_DOCKER_OS_VERSION}
$ docker build --no-cache --tag localndnsimbase:${NDNSIM_DOCKER_OS_VERSION} .
```

### ndnSIM image

See [fam4r/docker-ndnsim](https://github.com/fam4r/docker-ndnsim/blob/master/DEVELOPING.md#ndnsim-image).

## Updating the OS

The ["Downloading and Compiling ndnSIM" page](https://ndnsim.net/current/getting-started.html) reports the supported Operating Systems for ndnSIM.

If a new OS has been adopted or if the current OS version has been deprecated, create a new image:

- Create a folder for the new version: `mkdir ubuntu-20.04`
- Copy the previous version Dockerfile into the new folder `cp ubuntu-16.04/Dockerfile ubuntu-20.04`
- Edit the [dependencies](https://ndnsim.net/current/getting-started.html#prerequisites)
- build the image on a local instance
- build the ndnSIM on a local instance using the base OS image in the `FROM` command
- test a simulation, if it works commit and push