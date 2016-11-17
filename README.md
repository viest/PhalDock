[![Version 0.1](https://img.shields.io/badge/Version-0.1-brightgreen.svg)](https://github.com/VikinArtisan/PhalDock)
[![Phalcon master](https://img.shields.io/badge/phalcon-master-green.svg)](https://github.com/phalcon/cphalcon)
###Install

Clone this repository on your project root directory:

```bash
git clone git@github.com:VikinArtisan/PhalDock.git
```

###Usage

#####1、Build container

Run Containers: (Make sure you are in the PhalDock folder before running the docker-compose commands).D

```bash
docker-compose build
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

###On PhpStrom IDE development 

#####1、Use phpstrom open "PhalDock/workspace/application"

![image](https://github.com/VikinArtisan/PhalDock/blob/master/resource/Open.png)

#####2、Editor test.php

![image](https://github.com/VikinArtisan/PhalDock/blob/master/resource/Editor.png)

#####3、Refresh the localhost

![image](https://github.com/VikinArtisan/PhalDock/blob/master/resource/Localhost.png)