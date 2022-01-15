# Docker

* `docker system info` check docker infomation
* `docker --version` or`docker -v` check docker version

## image

* `docker image ls`  check download images

  * `-a` show a images
  * `--digests` show digests
  * `--filter dangling=true`
  * `--format "{{.Repository}}:{{.Tag}}:{{.Size}}"`
  * `-q` only show image id
* `docker image pull [image]:[version]` pull image from repo or dockerhub
* `docker search [image]` search image
* `docker image inspect [image]` see more image info

## container

* `docker container ls` check created containers ( all means see all containers )
* `docker container run -it --name [name] [image]` docker create new ubuntu container
* hello world
* `docker container exec -it [container] bash` attach in container
* `docker attach [container]` go into container
* `docker start [container]` start container
* `docker container stop [container]` stop container
* `docker container rm [container]` remove container
