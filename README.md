# Riot.im in Docker [![Build Status](https://travis-ci.org/bubuntux/docker-riot-web.svg?branch=master)](https://travis-ci.org/bubuntux/docker-riot-web)
This project is on charge of checking everyday if there is a new [Riot](https://riot.im) version and create the proper docker image and push it to the [hub](https://hub.docker.com/r/bubuntux/riot-web/) as need it.

# What is Riot ? #
[Riot](https://about.riot.im/what-is-riot) (formerly known as Vector) is a web client for [Matrix](https://matrix.org) an open network for secure, decentralized communication.

# How to use the docker image #
```
$ docker run --name riot -p 8080:80 -d bubuntux/riot-web
```
Then you can hit [http://localhost:8080](http://localhost:8080) in your browser.

# Riot configuration #
```
$ docker run -v /host/path/config.json:/etc/riot-web/config.json:ro --name riot -p 8080:80 -d bubuntux/riot-web
```
For information on the syntax of the riot configuration file, see [the official documentation](https://github.com/vector-im/riot-web#configjson).

# HTTP server configuration #
```
$ docker run -v /host/path/nginx.conf:/etc/nginx/nginx.conf:ro --name riot -p 8080:80 -d bubuntux/riot-web
```
For information on the syntax of the nginx configuration files, see [the official documentation](http://nginx.org/en/docs/) (specifically the [Beginner's Guide](http://nginx.org/en/docs/beginners_guide.html#conf_structure)).
