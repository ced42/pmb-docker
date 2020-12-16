# pmb-docker
Test [PMB software](https://www.sigb.net/index.php?lvl=cmspage&pageid=6&id_rubrique=220&opac_view=1) with Docker containers.

## Introduction

This project contains a docker-compose file to test quickly PMB software. It could be
interesting to test it before installing it on a server.

## How to

Follow these steps to test PMB:
- Clone or download this project, 
- Install [docker](https://docs.docker.com/get-docker/) and [docker-compose](https://docs.docker.com/compose/install/)
- Run in the folder corresponding to the cloned project:
```bash
docker-compose up -d
```
It will start 3 services :
- the webserver
- the db engine 
- one to connect to the db

It could be long the first time (depending on your internet speeed). Check if
all services are okay with:
```bash
docker-compose ps
```
Normally all services are "up".

## Try PMB

The Docker exposed port is 8080, so in your browser go to
"http://localhost:8080/pmb/tables/install.php" and it will ask you to install pmb.
The information are :
- db host: db
- db name: pmb
- db root password : password

After that, PMB will be available at "http://localhost:8080/pmb".



## Change version of PMB

If you want to test another version of PMB, change the values in the .env file.

