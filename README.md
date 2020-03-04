# docker-traefik-acme-portainer-vpn
Docker Infrastructure for a server with automatic SSL, portainer as a docker management client and VPN connection

## Installation
1. [Install docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
2. [Install docker-compose](https://docs.docker.com/compose/install/)
3. Pull this repository and cd into it
4. Run `docker network create traefik_network`. You can choose whatever name you want for the network.
5. Copy `acme.example.json` to `acme.json` and run `chmod 400 acme.json`
6. Copy `.env.example` to `.env` and update environment variables
7. Make sure your `PORTAINER_HOST` domain is pointing to your server (A record or CNAME record)
8. Run `docker-compose up -d`

If everything was correctly set up, you should be able to navigate to your `PORTAINER_HOST` and setup the username and password for the Portainer account.