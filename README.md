<br />
<p align="center">
  <h1 align="center">Wordpress Starter</h1>
</p>

## About The Project

This repository contains a simple and clean project with the files needed to start one or multiple wordpress websites on a server.

## Docker images used

### Reverse proxy
 - jwilder/nginx-proxy
 - jrcs/letsencrypt-nginx-proxy-companion
### Wordpress
 - mysql
 - wordpress

## Prerequisites

Make sure you have docker and docker-compose installed. If not, follow [this page](https://docs.docker.com/get-docker/)

Clone this repository:
```sh
git clone https://github.com/filipmanole/wordpress-starter.git
```

## Usage

```sh
docker network create nginx-proxy # this is the external network used by the containers
```

In the nginx directory, prepare the .env file. You can start from the existing .env.sample

```sh
cd nginx
cp .env.sample .env
vim .env # edit the file: set you email
```

After the you set the variables in .env file, start the reverse-proxy:

```sh
docker-compose up
```

In the wordpress directory, prepare the .env file. You can start from the existing .env.sample

```sh
cd wordpress
cp .env.sample .env
vim .env # edit the file: set your database, user, passwords and domain.
```

After the you set the variables in .env file, start the wordpress website:

```sh
docker-compose up
```

## Note

1. Instead the containers used for the wordpress website you can use containers with any other web application.
2. This repository can be used to start multiple wordpress websites, or host multiple web applications.