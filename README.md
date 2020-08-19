<br />
<p align="center">
  <h1 align="center">Two Wheels Self Balancing Robot</h1>
</p>

## About The Project

This repository contains the files needed to start one or multiple wordpress websites on a server.

## Docker images used

### Reverse proxy
 - jwilder/nginx-proxy
 - jrcs/letsencrypt-nginx-proxy-companion
### Wordpress
 - mysql
 - wordpress

## Prerequisites

Make sure you have docker and docker-compose installed.

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
vim .env #edit the file
```

After the you set the variables in .env file, start the reverse-proxy:

```sh
docker-compose up
```

In the wordpress directory, prepare the .env file. You can start from the existing .env.sample

```sh
cd wordpress
cp .env.sample .env
vim .env #edit the file
```

After the you set the variables in .env file, start the wordpress website:

```sh
docker-compose up
```

## Note

1. Instead the containers used for the wordpress website you can use containers with any other web application.
2. This repository can be used to start multiple wordpress websites, or host multiple web applications.