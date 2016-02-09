# shellcheck-docker

Generating an updated shellcheck binary for ubuntu from a Docker container.

## How to

```console
$ docker build -t shellcheck .
$ docker run -t shellcheck cat ~/.cabal/bin/shellcheck > shellcheck
```
