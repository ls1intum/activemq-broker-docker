# activemq-broker-docker

This repository hosts the packages for [activemq-artemis](https://github.com/apache/activemq-artemis).

These images are built for each release:
- `ghcr.io/ls1intum/activemq-broker-docker-debian:RELEASE_VERSION`
- `ghcr.io/ls1intum/activemq-broker-docker-centos:RELEASE_VERSION`
- `ghcr.io/ls1intum/activemq-broker-docker-adoptopenjdk-11:RELEASE_VERSION`

`RELEASE_VERSION` is the release version of activemq-artemis (e.g. `2.21.0`).

## Publish new images
Create a new Release in GitHub and use the wanted `RELEASE_VERSION` as tag.

## How it works
This repository contains a GitHub action, which clones the [activemq-artemis](https://github.com/apache/activemq-artemis) repository and executes the steps listed [here](https://github.com/apache/activemq-artemis/tree/main/artemis-docker).

The action is only triggered on new tags.