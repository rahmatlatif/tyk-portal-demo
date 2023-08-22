# Tyk Enterprise Portal using Docker
## Quick start

**Prerequisites**

- [Docker](https://docs.docker.com/get-docker/)
- Running Tyk Pro deployment (To synchronize API plans and products)

  You can use [Tyk Pro Docker Demo](https://github.com/TykTechnologies/tyk-pro-docker-demo) for PoC purposes

Run these commands:

1. `git clone https://github.com/rahmatlatif/tyk-portal-demo && cd tyk-portal-demo`

2. `docker-compose up`

3. `docker network connect <tyk pro network> <tyk portal container name>`

By default the `tyk pro network` would be `tyk-pro-docker-demo_tyk` and `tyk portal container name` would be `tyk-portal-demo-tyk-portal-1`

You can list docker networks using:
`docker network ls`

You can list docker containers using:
`docker container ps`

4. Navigate to [http://localhost:3001](http://localhost:3001) and input the admin registration details.

## Synchronize Tyk Pro to Tyk Portal

If using [Tyk Pro Docker Demo](https://github.com/TykTechnologies/tyk-pro-docker-demo) set Dashboard URL to http://tyk-dashboard:3000

If not using Tyk Pro Docker Demo, set Dashboard URL

## Advanced

### Cleanup Docker Containers

To delete all docker containers as well as remove all volumes from your host:

```
$ docker-compose down -v
```

