[<img src="https://hotio.dev/img/conreq.png" alt="logo" height="130" width="130">](https://github.com/archmonger/conreq)

[![GitHub Source](https://img.shields.io/badge/github-source-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/hotio/conreq)
[![GitHub Registry](https://img.shields.io/badge/github-registry-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/orgs/hotio/packages/container/package/conreq)
[![Docker Pulls](https://img.shields.io/docker/pulls/hotio/conreq?color=ffb64c&style=flat-square&label=pulls&logo=docker&logoColor=white&labelColor=757575)](https://hub.docker.com/r/hotio/conreq)
[![Discord](https://img.shields.io/discord/610068305893523457?style=flat-square&color=ffb64c&label=discord&logo=discord&logoColor=white&labelColor=757575)](https://hotio.dev/discord)
[![Upstream](https://img.shields.io/badge/upstream-project-ffb64c?style=flat-square&labelColor=757575)](https://github.com/archmonger/conreq)
[![Website](https://img.shields.io/badge/website-hotio.dev-ffb64c?style=flat-square&labelColor=757575)](https://hotio.dev/containers/conreq)

## Starting the container

CLI:

```shell
docker run --rm \
    --name conreq \
    -p 8000:8000 \
    -e PUID=1000 \
    -e PGID=1000 \
    -e UMASK=002 \
    -e TZ="Etc/UTC" \
    -v /<host_folder_config>:/config \
    hotio/conreq
```

Compose:

```yaml
version: "3.7"

services:
  conreq:
    container_name: conreq
    image: hotio/conreq
    ports:
      - "8000:8000"
    environment:
      - PUID=1000
      - PGID=1000
      - UMASK=002
      - TZ=Etc/UTC
    volumes:
      - /<host_folder_config>:/config
```

## Tags

Go [here](https://hotio.dev/tags-overview/#hotioconreq) to see all available tags.
