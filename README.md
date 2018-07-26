# Traefik Socat Demo

This repo provides the stack files for the blog post found at [https://blog.mikesir87.io/2018/07/letting-traefik-run-on-worker-nodes/](https://blog.mikesir87.io/2018/07/letting-traefik-run-on-worker-nodes/). Go read the post to find out what this is all about.

## Commands

```bash
docker network create --attachable --driver overlay app-entry
docker network create --attachable --driver overlay mgmt
docker stack deploy -c proxy-stack.yml proxy
docker stack deploy -c app-stack.yml cats
``` 

