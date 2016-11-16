###Install

Clone this repository on your project root directory:

```bash
git clone git@github.com:VikinArtisan/PhalDock.git
```

###Usage

#####1、Build container

Run Containers: (Make sure you are in the PhalDock folder before running the docker-compose commands).D

```bash
docker-composer build
```
#####2、Running container

```bash
docker-compose up -d nginx php-fpm workspace
```
#####3、Enter the Workspace container

```bash
docker-compose exec workspace bash
```

###Stop

#####1、Close all running Containers

```bash
docker-compose stop
```
#####2、To stop single container 

```bash
docker-compose stop {container-name}
```