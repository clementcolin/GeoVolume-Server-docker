# GeoVolume-Server-docker

The docker container associated to the GeoVolume-Server web application.

Build the docker image with

```bash
docker build -t vcity:geovolume-server Context
```

Then run the container e.g. with

```bash
docker run -p 0.0.0.0:8080:3000/tcp [--detach] --rm -t vcity:geovolume-server
```

and open a web browser on URL `http://localhost:8080/`
