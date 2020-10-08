# TeXstudio-docker
```bash
docker build \
    --no-cache \
    --build-arg IMAGE_VERSION=unstable-slim \
    --file Dockerfile.debian \
    --tag image-name:version .
```
```bash
docker volume create \
    --driver local \
    --name volume-name
```
```bash
xhost +local:docker
```
```bash
docker container run \
    --interactive \
    --tty \
    --volume /tmp/.X11-unix:/tmp/.X11-unix \
    --mount source=volume-name,target=/texstudio \
    --env DISPLAY=unix$DISPLAY \
    --name container-name image-name:version
```
