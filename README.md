# Ghost Server

A simple compose file to start up a [ghost](https://ghost.org) site
with an auto renewing [A+ ranked cert](https://www.ssllabs.com/ssltest/analyze.html?d=mattflow.codes)
verified by letsencrypt

Example site using this config: https://mattflow.codes

## Prerequsites

1. Docker and docker-compose are installed on the host server
2. Proper DNS records are configured for your domain

**Note:** Remove `,www.${DOMAIN}` from `VIRTUAL_HOST` and `LETSENCRYPT_HOST` if you don't plan on setting up a www subdomain.

## Set up

1. Log into your server
2. Clone this repo and enter the directory

```
git clone https://github.com/mattflow/ghost-server.git
cd ghost-server
```

3. Add a `.env` file with `DOMAIN` and `EMAIL` variables

```
DOMAIN=yourdomain.com
EMAIL=you@yourdomain.com
```

4. Run compose up

```
docker-compose up -d
```

5. Set up your site at `https://<your domain>.com/ghost`
