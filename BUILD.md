## Impulse Build Guide

### setup

#### install docker
```
brew cask install docker
```

### build local docker images
```
cd $IMPULSE_HOME
export IMPULSE_VERSION=1.11.0

docker build -t impulse/python2-base docker/python2-base
docker build -t impulse/python2-dev docker/python2-dev
docker build -t impulse/python2 docker/python2
docker build -t impulse/python3-base docker/python3-base
docker build -t impulse/python3-dev docker/python3-dev
docker build -t impulse/spark docker/spark
docker build -t impulse/impulse .
docker build -t impulse/impulse-ml:$IMPULSE_VERSION impulse-ml
docker build -t impulse/impulse-ml-py:$IMPULSE_VERSION -f impulse-ml/Dockerfile_py impulse-ml
docker build -t impulse/impulse-tools:$IMPULSE_VERSION impulse-tools
docker build -t impulse/impulse-streaming:$IMPULSE_VERSION impulse-streaming
docker build -t impulse/impulse-ui:$IMPULSE_VERSION impulse-ui
docker build -t impulse/impulse-gw:$IMPULSE_VERSION impulse-gw
docker build -t impulse/impulse-manage:$IMPULSE_VERSION scripts
docker build -t impulse/impulse-factor:$IMPULSE_VERSION impulse-factor
docker build -t impulse/impulse-defective:$IMPULSE_VERSION impulse-defective
docker build -t impulse/zk:$IMPULSE_VERSION zk
docker build -t impulse/kafka:$IMPULSE_VERSION kafka
docker build -t impulse/superset:$IMPULSE_VERSION superset
```
