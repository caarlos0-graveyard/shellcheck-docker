# shellcheck-docker

Generating an updated shellcheck binary for ubuntu from a Docker container, battle-tested
on [caarlos0/shell-ci-build](https://github.com/caarlos0/shell-ci-build).

## How to

```console
$ docker build -t shellcheck .
$ docker run -t shellcheck
$ ls
# ...
shellcheck*
```
