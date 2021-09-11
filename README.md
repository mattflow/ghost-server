# Ghost Server

A simple compose file to start up a ghost site
with auto renewing certs verified by letsencrypt

## Prerequsites

1. Docker and docker-compose are installed on the host server
2. Proper DNS records are configured for your server and domain

__Note:__ Remove `www.${DOMAIN}` from `VIRTUAL_HOST` and `LETSENCRYPT_HOST` if you don't plan on setting up a www subdomain.

## Set up

1. Log into your server
2. Clone this repo and enter the directory 

```
git clone https://github.com/mattflow/ghost-server.git
cd ghost-server
```

3. Add a .env file with `DOMAIN` and `EMAIL` variables

```
DOMAIN=yourdomain.com
EMAIL=you@yourdomain.com
```

4. Run compose up

```
docker-compose up -d
```