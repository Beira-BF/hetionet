## Building the docker

```sh
TAG="dhimmel/hetionet:hetionet-v1.0_neo4j-3.0.2"
docker build --tag $TAG --file Dockerfile .
```

## Running the docker

For development (maps port 7474 to port 7474):

```sh
docker run --publish=7474:7474 --volume=$HOME/neo4j/hetionet-data:/data $TAG
```

For deployment (maps port 7474 to port 80):

```sh
#docker run --detach --publish=80:7474 --volume=$/neo4j-data-volume:/data $TAG
```

## On docker hub

https://hub.docker.com/r/dhimmel/hetionet/

## Browse live instance at

http://neo4j.het.io
