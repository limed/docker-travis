# docker-travis
Dockerize travis cli tool

## usage
To build

```
$ docker build -t <username>/travis .
$ docker push <username>/travis
```

To use

```
$ docker run --rm -it -w /code -v $(pwd):/code <username>/travis:latest help
```

You can also create a bash function for this

```
function travis() {
	docker run --rm -it -w /code -v $(pwd):/code <username>/travis:latest "${@}"
}
```
