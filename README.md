# Secured by OAuth2 Unleash on Docker

## Run with docker
We have set up docker-compose to start 

* [Postgres](https://www.postgresql.org/)
* [Unleash server](github.com/Unleash/unleash)
* [OAuth2 Proxy](https://github.com/bitly/oauth2_proxy)

This makes it really fast to start up unleash locally without setting up a database or node.

### Requirements
We are using docker-compose version 3.3 and it requires:

- Docker engine 17.06.0+
- docker-compose 1.14.0+

For more info, check out the compatibility matrix on Docker's website: [compatibility-matrix](
https://docs.docker.com/compose/compose-file/compose-versioning/#compatibility-matrix)

### Usage

1. Create your app in Azure, Google, Github or other auth provider listed [here](https://github.com/bitly/oauth2_proxy#oauth-provider-configuration).

2. Change to your app specific:

* `OAUTH2_PROXY_CLIENT_ID`
* `OAUTH2_PROXY_CLIENT_SECRET`
* Other specific [OAuth2 Proxy](https://github.com/bitly/oauth2_proxy#command-line-options) options like `--azure-tenant`

3. Run

```bash
$ docker-compose build
$ docker-compose up
```

And have fun with secured feature toggling app :smile:
