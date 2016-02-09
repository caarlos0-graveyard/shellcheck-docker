# shellcheck-docker

Generating an updated shellcheck binary for ubuntu from a Docker container, battle-tested
on [caarlos0/shell-ci-build](https://github.com/caarlos0/shell-ci-build).

## How to

### Check your scripts

```console
$ docker run \
  -v /folder/with/my/scripts:/tmp \
  -t caarlos0/shellcheck \
  sh -c 'shellcheck /tmp/*.sh'
```

### Copy the binary to outside

So you can use in it any ubuntu machine, travis machines, for example,
as I do in [caarlos0/shell-ci-build](https://github.com/caarlos0/shell-ci-build).

```
$ docker run \
  -v `pwd`:/tmp \
  -t caarlos0/shellcheck \
  cp -f /usr/bin/shellcheck /tmp/
```

### Build

Not really needed unless you change something, as this repo is an automated Docker hub build.

```console
$ docker build -t caarlos0/shellcheck .
```
