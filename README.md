Find the IMAGE ID of a specific TAG on Docker Hub. Helpful to know if you have the same version locally or if you should consider to update.

Two versions available, depending on what you have installed (`python` or `jq`).

Example:
```
$ ./docker-hub-image-id library/ubuntu bionic
775349758637
$ ./docker-hub-image-id --full library/ubuntu bionic
775349758637aff77bf85e2ff0597e86e3e859183ef0baba8b3e8fc8d3cba51c
```
