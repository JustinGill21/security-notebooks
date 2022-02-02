# security-notebooks
To launch a jupyter stack datascience notebook:

```bash
docker run --rm -it -p 10000:8888 -v "${PWD}:/home/jovyan/work" jupyter/datascience-notebook:b418b67c225b
```

Note: the above will be available at localhost:10000

Do the same for `docker-compose.yml` file:

```bash
docker-compose up -d
```

I've uploaded a public docker image to dockerhub where it can be pulled from any machine using the command

```bash
docker pull justingill/my-datascience-notebook
```
