# security-notebooks
This project explores how to create customizable python environments with docker. Docker images can be saved publicly and pulled to any environment.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/JustinGill21/security-notebooks/HEAD)

The built image is [hosted on Docker-Hub](https://hub.docker.com/repository/docker/justingill/my-datascience-notebook)


To launch a jupyter stack datascience notebook, use docker run command:

```bash
docker run --rm -it -p 10000:8888 -v "${PWD}:/home/jovyan/work" jupyter/datascience-notebook:b418b67c225b
```
Note: the above will be available at localhost:10000

## Using this repository
### With docker,

Build:

```bash
docker build --rm -t jupyter/my-datascience-notebook .
# - this command builds the docker image with the Dockerfile
# specifications for the container, given the requirements
# stated in the requirements.txt file
```

To Run:

```bash
docker run --rm -it -p 8888:8888 jupyter/my-datascience-notebook
# - Should publish port 8888
# - Should mount the local directory as a volume in the
#   container's home directory
# - Should `--rm` container when done
# - Should use `-it` mode
```

To build and run with docker-compose, use command:

```bash
docker-compose up -d
# - It should publish port 8888
# - It should mount the local directory as a volume in the container's
#   home directory
```

I've uploaded a public docker image to dockerhub where it can be pulled from any machine using the command

```bash
docker pull justingill/my-datascience-notebook
```
