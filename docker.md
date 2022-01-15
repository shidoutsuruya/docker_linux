# Docker

* `docker login` log in docker repo
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
* `docker image rm [image]` or `docker rmi [image]` remove image
* `docker image build -t [dockerfile]` build my new image
* `docker image push [new_image]` push your image into hub
* `docker image history [image]` see image history

## container

* `docker container ls` check created containers ( all means see all containers )
  * `-a` show all container
* `docker container run -it [image]` docker create new ubuntu container
  * `--restart` restart the container
  * `--name [name]` define the name of container
  * `-p 80:8080` give port
  * `-d` run but not attach in container
* `docker container exec -it [container] bash` attach in container
* `docker attach [container]` go into container
* `docker start [container]` start container
* `docker container stop [container]` stop container
* `docker container rm [container]` remove container
