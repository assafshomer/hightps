# hightps

## Dach
### Build docker image
```
  git clone
  cd dach
	docker build -t dach .
```
### Run docker container
#### Daemon
```
  docker run -d dach
```
#### Interactive shell
```
  docker run -it dach /bin/bash
```
So far all I can get out of this is "Started successfully", not sure what the next step is