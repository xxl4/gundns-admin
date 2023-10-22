# Installation on docker

The Docker image is gundnsadmin/pda-legacy available on [DockerHub](https://hub.docker.com/r/gundnsadmin/pda-legacy)

The supported environment variables to configure the container are located [here](../configuration/Environment-variables.md).

You can run the container and expose the web server on port 9191 using:
```bash
docker run -d \
    -e SECRET_KEY='a-very-secret-key' \
    -v pda-data:/data \
    -p 9191:80 \
    gundnsadmin/pda-legacy:latest
```
