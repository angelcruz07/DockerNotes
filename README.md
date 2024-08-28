# Docker

## Download Images

```bash
docker image pull debian
```

## List images

```bash
docker image list

docker image ls

docker images
```

## New Container

```bash
docker container create --name debian-test debian

#Options

```

## View Containers

```bash
docker container list

#View all containers
docker container list --all

# Shortcuts

docker container ls -a

docker ps

docker ps -a
```

> [TIP]
> If you have no idea what docker command does, you can write it by
> adding --help at the end.

## Run Container

```bash
docker container start debian-test
```

Creating the container in the previous way we
have a problem since there is no standard input (STDIN) & (tty)
in this case **bash** which is a problem when
wanting to interact with the container so we should
create it in the following way.

```bash
 docker container create --interactive --tty --name debian-shell debian
```

## Start Container Interactive & tty

```bash
docker container start  --interactive debian-shell

##Shortcuts
docker start -i debian-shell
```
