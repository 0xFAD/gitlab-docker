# Gitlab docker
This is an example of how to configure a Gitlab server by separating some of the integrated components.

You need to have a working **NGINX** server to proxy at **172.19.0.1: 8080**.

## How to run
```
git clone git@github.com:0xFAD/gitlab-docker.git
cd gitlab-docker && docker-compose -d up
```

This will initialize a docker network and the following containers:
- [gitlab:latest](https://hub.docker.com/_/gitlab-community-edition) (gitlab_server)
- [redis:alpine](https://hub.docker.com/_/redis) (gitlab_redis)
- [postgres:alpine](https://hub.docker.com/_/postgres) (gitlab_db)

This wants to be a simple example, for more information on the configuration of Gitlab, see the official [documentation](https://docs.gitlab.com/).
