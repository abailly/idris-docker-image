# Docker image for [Idris lang](http://www.idris-lang.org/)

The image is available on dockerhub: [dgellow/idris](https://hub.docker.com/r/dgellow/idris/)
Based on [_/haskell](https://hub.docker.com/r/_/haskell/), latest idris installed and compiled via cabal.

# Usage

From the cli:

```
$ docker run dgellow/idris idris --help
```

From a `Dockerfile`:

```
FROM dgellow/idris

ADD . /app
WORKDIR /app

RUN idris main.idr -o hello.o
CMD ["/app/hello.o"]
```