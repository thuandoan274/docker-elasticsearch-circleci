# docker-elasticsearch-circleci

Docker Image for Circle CI Build

# Feature

- disable Bootstrap check
  - https://discuss.circleci.com/t/running-elasticsearch-5/8559/7
- disable X-Packs Security
  - because it is not required for CI environment
- install minimal plugins
  - analysis-kuromoji

# Docker Hub

https://hub.docker.com/r/kenju/elasticsearch-circleci/

# Usage

```bash
docker pull kenju/elasticsearch-circleci
```

# Development

## Publish to Docker Hub

```bash
docker login
VER=0.1
TAG=kenju/elasticsearch-circleci:$VER
docker build -t $TAG
docker push $TAG
```
