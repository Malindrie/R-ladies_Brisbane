### Creating a Base R docker

To build the image use:

``` shell
docker build . -t maldharm/baser:410
```
Build arguments:

* `.` - enables to use any file in the root folder
* `-t` - Name and optionally a tag in the `name:tag` format
* `docker build` arguments documentation - https://docs.docker.com/engine/reference/commandline/build/

Where `maldharm` is the Docker Hub address, `baser` is the image name, and `410` is the image tag. You can use also `docker build . -t baser:410`, but then you will have to retag it before pushing it to Docker Hub


To push the docker to Docker Hub use:

```
docker push maldharm/baser:410
```

The image is available over [here](https://hub.docker.com/repository/docker/maldharm/baser)

To launch the container use:

``` shell
docker run -t -d maldharm/baser:410
```

* `-t` - Allocate a pseudo-TTY
* `-d` - Run container in background and print container ID
* `docker run` arguments documentation - https://docs.docker.com/engine/reference/commandline/run/

To access the container while running use:

``` shell
docker exec -it container_id /bin/sh
```

To get the `container_id` use `docker container ps`

To view the metadata of the image:
```
docker inspect maldharm/baser:410
```
