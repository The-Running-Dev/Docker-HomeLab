# Docker-HomeLab

A collection of Docker Compose files used in my home lab. Available on GitHub so they can be consumed through GitOps in Portainer or alike container management software.

https://github.com/The-Running-Dev/Docker-HomeLab/

## Available Services

### Portainer Agent

```portainer-agent/docker-compose.yml``` The compose file for the Portainer agent. No configuration is needed, runs as is, and it is meant to be used with Linux based containers. Documentation is at <https://docs.portainer.io/v/2.15/start/install/agent/docker/linux>.

### Portainer Server

```portainer-server/docker-compose.yml``` The compose file for the Portainer server. Configuration is done through the ```.env``` file. Documentation is at <https://docs.portainer.io/v/2.15/start/install/server/docker/linux>.

```portainer-server/.env``` The environment configuration for the Portainer server compose, mostly self explanatory. Note: This deployment supports access both over HTTP and HTTPs (with self signed certificate inside the container). If you want to use your own SSL certificate, the documentation is at <https://docs.portainer.io/advanced/ssl>.

### Watchtower

```watchtower/docker-compose.yml``` The compose file for the Watchtower services. This includes ```containrrr/watchtower```, for auto-updating container images; and also ```willfarrell/autoheal``` for health check and auto-heal support (<https://docs.docker.com/compose/compose-file/compose-file-v3/#healthcheck>).