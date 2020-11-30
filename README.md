# TDLight Telegram Bot API traefik deployment

This repository contains the necessary compose files for
deploying [TDLight Telegram Bot API](https://github.com/tdlight-team/tdlight-telegram-bot-api)
in a production environment.

## Requirements
- Docker
- docker-compose
- 80 and 443 port access

## Usage
1. Edit the files `traefik.conf`, `botapi.conf` and `traefik/confs/middlewares.conf` with your domains and passwords
2. Enter `traefik/` and run `docker-compose up -d`
3. Enter `botapi/` and run `docker-compose up -d`

## Tips
- If you already use another reverse proxy service or your ports are already used by another proccesses update 
the configuration accordingly
- You need access to Docker socket, check the permissions
- Check the DNS records
- Don't use the "Cloudflare orange cloud" for the botapi domain. Free accounts are limited to max 50MB per request. 
Cloudflare is useless for this setup anyway.

