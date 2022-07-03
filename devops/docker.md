# Docker

- [Home](https://www.docker.com/)

## Videos

- [Docker Tutorial for Beginners - Programming With Mosh](https://www.youtube.com/watch?v=pTFZFxd4hOI)

## Guidelines

Docker configuration files should be placed inside the docker folder in the project root, so as to better organize Docker files or file overrides. For each project it is recommended to declare **three files** for the container configuration:

- `docker-compose.yml`: contains the general configuration of the containers. Here, no reference should be made to the port configurations or the local environment
- `docker-compose.override.yml.dist`: contains the default configuration of the ports or other configurations related to the environment. This file must be committed together with the docker-compose.yml
- `docker-compose.override.yml`: contains the configuration of the ports of the local environment. Any configuration inserted within this file will overwrite the one present in the - docker-compose.yml file. For this reason, this file must NOT be committed and must be inserted within the .gitignore.