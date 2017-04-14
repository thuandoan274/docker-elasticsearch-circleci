# docker-elasticsearch-circleci

Docker Image for Circle CI Build

# Feature

- disable Bootstrap check
  - https://discuss.circleci.com/t/running-elasticsearch-5/8559/7
- disable X-Packs Security
  - because it is not required for CI environment

# Docker Hub

https://hub.docker.com/r/kenju/elasticsearch-circleci/

# Usage

```bash
docker pull kenju/elasticsearch-circleci
```
