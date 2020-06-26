# docker-traefik-acme-portainer-vpn
Docker Infrastructure for a server with automatic SSL, portainer as a docker management client and VPN connection

## Installation

Make sure you generate your self-signed certificates: [README](cert/README.md)

### For servers with self-signed certificates
1. [Install docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
2. [Install docker-compose](https://docs.docker.com/compose/install/)
3. Pull this repository and cd into it
4. Run `docker network create traefik_network`. You can choose whatever name you want for the network.
6. Copy `.env.example` to `.env` and update environment variables
8. Run `docker-compose up -d`

If everything was correctly set up, you should be able to navigate to your `PORTAINER_HOST` and setup the username and password for the Portainer account.

## Other components
1. [Wordpress](/wordpress) - Add a Wordpress installation to your host in seconds!