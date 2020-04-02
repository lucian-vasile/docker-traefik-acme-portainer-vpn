# wordpress on docker-traefik-acme-portainer-vpn infrastructure
Fast way to have a wordpress installation on docker infrastructure with automatic SSL and minimum configuration

It's dev and production-ready.

## Installation
1. Copy `.env.example` to `.env`
2. Update `TRAEFIK_NETWORK` to match the network used by your traefik instalation. You can check the name by running `docker network ls`
3. Update the `APP_DOMAIN` to whatever domain you're using. Make sure the domain and www subdomain are both pointing (A and/or CNAME record) to the current server
4. Update the `DOCKER_RULES_GROUP` with an unique identifier on this traefik installation
5. (Optional but recommended) Update the `MARIADB CONF` section for security reasons
6. Run `docker-compose up` or `docker-comppose up -d`

If everything was correctly set up, you should be able to navigate to your `APP_DOMAIN` and setup Wordpress.