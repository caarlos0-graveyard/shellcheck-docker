# shellcheck-docker

Generating an updated shellcheck binary for ubuntu from a Docker container, battle-tested
on [caarlos0/shell-ci-build](https://github.com/caarlos0/shell-ci-build).

## How to

```console
# build the image:
$ docker build -t shellcheck .

# run it locally against your scripts:
$ docker run -v /folder/with/my/scripts:/tmp -t shellcheck sh -c 'shellcheck /tmp/*.sh'

# copy the binary to outside, so it can be used in any ubuntu machine:
$ docker run -v `pwd`:/tmp -t shellcheck cp -f /usr/bin/shellcheck /tmp/
```
