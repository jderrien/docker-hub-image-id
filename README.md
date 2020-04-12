For some reasons, Docker Hub doesn't the IMAGE ID of an image.

These tools help to find the IMAGE ID of a specific TAG on Docker Hub. Convenient to know if you have the same version locally or if you should consider to upgrade.

Example:
```
$ ./docker-images-check-tag-updates
✓ puckel/docker-airflow:1.10.6-1 | local: f98ecb2f13d2 | hub: f98ecb2f13d2 (https://hub.docker.com/r/puckel/docker-airflow)
✕ python:3.6-slim-stretch | local: 60ebf45b20e2 | hub: fa7acd99a1d8 (https://hub.docker.com/_/python)
✕ ubuntu:bionic | local: 775349758637 | hub: 4e5021d210f6 (https://hub.docker.com/_/ubuntu)
```

`docker-hub-image-id` can be used directly as follow:
```
$ ./docker-hub-image-id puckel/docker-airflow 1.10.6-1
f98ecb2f13d2

$ ./docker-hub-image-id python 3.6-slim-stretch
fa7acd99a1d8

$ ./docker-hub-image-id --full python 3.6-slim-stretch
fa7acd99a1d859ffddeda1c3c93c7009f84b2c7db0f4426e98b3931413b28d82
```

Requirements:
- `curl`
- `jq` or `python` (for json parsing)

Optional env variables:
- `JSON_PARSER=<path>` (where `<path>` is the path to a `python` or `jq` executable)
- `DEBUG=1` to enable debug mode
