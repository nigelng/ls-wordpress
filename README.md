# Wordpress for Lightsail Container

These images are based on [Wordpress images](https://hub.docker.com/_/wordpress), with custom.ini include

## Wordpress 6 [`6` `latest`]

The `6` tag includes:

- wordpress 6

## Development

### Create dockerx builder

```
docker buildx create --use
```

### Build Image

```sh
docker build -f <version>/Dockerfile -t nigelng/ls-wordpress:<tagname> .
```

```sh Build Image for amd64
docker buildx build --platform linux/amd64 -t nigelng/ls-wordpress:6 .
```

### Run Image

```sh
docker run -it nigelng/ls-wordpress:<tagname> bash
```

### Push to DockerHub

```sh
# Push all new tags
docker push --all-tags nigelng/ls-wordpress

# Push particular tag
docker push -t nigelng/ls-wordpress:<tagname>
```
