# Docker

## Overview.

- Tries to make it really easy to run your code on any machine, local or on the cloud.
- Docker allows you to containerize running processes, running the code in a configured, self-contained “container" that has all the necessary dependencies installed.
- There are docker images, which are files that have dependencies and configuration to run a program.
	- We can run or spin up an image, and this image will be a running instance in a container.

## Common commands.

```sh
docker run [-it] <image> [custom-entry-command]
```

- Tells Docker to spin up an instance of `image`, with an optional entry command.
	- If we use `-it` with a custom command of `sh`, we can open a new container straight into the shell.
- Docker will fetch the image from DockerHub if this is the first time running this image.
- This is really just a combination of `docker create` and `docker start`.

```sh
docker start [-a] <instance-id>
```

- Starts an instance that was previously created.
- Can be used to run a container that was previously shut down.
- `-a` flag forwards output from the instance to the currently open terminal instance.
	- “attach" your terminal to the Docker instance.

```sh
docker ps [--all]
```

- Shows all running Docker instances.
- `--all` flag shows all Docker instances, including ones that have been terminated already.

```sh
docker exec [-it] <container-id> <command>
```

- Used to execute a command inside a running container.
- `-it` lets you type input directly into the container.
	- `-i` redirects your input to `STDIN` of the container.
	- `-t` makes the output actually nice and useable.
- Can set the `<command>` as `sh` to just work in the container as normal.

```sh
docker logs <container-id>
```

- Output the past logs of the container into your terminal.

```sh
docker stop <container-id>
docker kill <container-id>
```

- `stop` sends a `SIGTERM` signal, allows for time to cleanup.
	- Prefer this method!
- `kill` sends a `SIGKILL` signal, no time for cleanup.

```sh
docker rmi <image-name>
```

- manually remove an image or tag.

```sh
docker system prune
```

- Clear all old Docker containers.

## Creating images.

- We will create a Dockerfile.
- Through some magic, the Docker client and server will create a useable image.

### Example redis-server image.

```Dockerfile
# Use an existing docker image as a base
FROM alpine

# Download and install a dependency
RUN apk add --update redis

# Tell the image what to do when it starts
CMD ["redis-server"]
```

- After creating the above Dockerfile, we run:

```sh
docker build [-t <docker-username/project-name:version>] <filepath-containing-Dockerfile>
```

- `-t` allows us to tag our builds, letting us refer to the images as the tag names.
- Intermediate containers.
	- The image from the previous step is temporarily spun up, in order to perform the next step!
		- After one step is run, a new image is created with the state of running that step!
		- We chain these intermediate images/containers together until we reach the end of the Dockerfile.
	- On rebuilds, intermediate containers that don’t need to be changed are cached and reused.
		- Try to order Dockerfile updates to take advantage of these caches.

```sh
docker run [-p LOCAL:CONTAINER] <container-id
```

- Can forward local ports to point to ports inside the Docker container.
