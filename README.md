# TiddliWiki 5 Docker image

Run TiddlyWiki 5 via Docker.

Forked from
[m0wer/tiddlywiki-docker](https://github.com/m0wer/tiddlywiki-docker) to add a ``docker-compose`` file.

The Docker image is available at [m0wer/tiddlywiki - Docker
Hub](https://hub.docker.com/r/m0wer/tiddlywiki).

## Available Docker Images at DockerHub

Image Name       | Tag        | TiddyWiki Version
-----------------|------------|------------------
m0wer/tiddlywiki | latest     | 5.2.0
m0wer/tiddlywiki | v[X]       | [X]
m0wer/tiddlywiki | test       | ?

## Prerequisites

* Docker.

## Keeping the data

Edit ``docker-compose.yml``, replacing ``/home/example/tiddlywiki`` with the path to your tiddlywiki directory.

## Authentication

To enable authentication, simply provide the
`USERNAME` and `PASSWORD` environment in the ``variables.env`` file.

## Quickstart

```bash
docker-compose up -d
```

Now TiddlyWiki should be running on
[http://localhost:8080](http://localhost:8080).

## Stop server

```bash
docker-compose down
```

## Other settings

### Limit Node.js memory

If you are in a memory-constrained environment, you can provide the
`NODE_MEM` environment variable to specify the memory ceiling (in MB and in ``variables.env``).

### Debug

Set the `DEBUG_LEVEL` environment variable to `debug` (also in ``variables.env``).
