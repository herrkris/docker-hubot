docker-hubot
============

[![Docker Hub](https://img.shields.io/badge/docker-mkaag%2Fhubot-008bb8.svg)](https://registry.hub.docker.com/u/herrkris/docker-hubot/)

This repository contains the **Dockerfile** and the configuration files to build [Hubot](https://hubot.github.com/) for [Docker](https://www.docker.com/).

### Base Docker Image

* [node slim](https://github.com/joyent/docker-node)

### Hubot Script

* hubot-auth
* hubot-codinglove
* hubot-diagnostics
* hubot-gitlab-hooks
* hubot-google-images
* hubot-google-translate
* hubot-help
* hubot-maps
* hubot-motivate
* hubot-newrelic2
* hubot-pugme
* hubot-redis-brain
* hubot-azure-scripts
* hubot-rules
* hubot-seen
* hubot-shipit
* hubot-slack
* hubot-thank-you
* hubot-youtube
* hubot-slack-relay


### Installation

```bash
docker build -t herrkris/docker-hubot github.com/herrkris/docker-hubot
```

### Environment Variables

* HUBOT_NAME
* HUBOT_SLACK_TOKEN
* HUBOT_AUTH_ADMIN
* GITLAB_CHANNEL
* GITLAB_DEBUG
* GITLAB_BRANCHES
* GITLAB_SHOW_COMMITS_LIST
* GITLAB_SHOW_MERGE_DESCRIPTION
* HUBOT_NEWRELIC_API_KEY
* HUBOT_NEWRELIC_API_HOST
* HUBOT_BRAIN_AZURE_STORAGE_ACCOUNT
* HUBOT_BRAIN_AZURE_STORAGE_ACCESS_KEY

### Usage

#### Basic usage

```
docker run -v /home/user/hubot_scripts:/opt/scripts \
--link redis:redis \
-p 8080:8080 \
herrkris/docker-hubot
```
