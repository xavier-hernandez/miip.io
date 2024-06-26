
# miip.io

## Fork of ifconfig.io
This is a fork of ifconfig.io. Please read the original repo for more configuration instructions.

Original code: https://github.com/georgyo/ifconfig.io/

Original website: https://ifconfig.io/

## My Enhancements
- Maxmind
  - Geo Location API or Local databases
- Plausible Analytics

This repo: https://github.com/xavier-hernandez/miip.io

Docker Image: https://hub.docker.com/r/xavierh/miip

Website: https://miip.io/

## Docker-Compose

Here is a sample docker-compose file:

``` bash
version: "3.4"

services:
  miip:
    container_name: miip
    image: xavierh/miip:latest
    ports:
      - 8080:8080
    environment:
      HOSTNAME: "miip.io"
      MAXMIND_USERNAME: [USERNAME] #internal GeoLite2 databases are used if your not passing a username or password 
      MAXMIND_PASSWORD: [PASSWORD] #internal GeoLite2 databases are used if your not passing a username or password
      PLAUSIBLE: [PLAUSIBLE_DOMAIN] #entering a domain here will enable the snippet
      PLAUSIBLE_SELF_HOSTED_DOMAIN: [PLAUSIBLE_SELF_HOSTED_DOMAIN] #meant to set the JS script to your self hosted domain
      FORWARD_IP_HEADER: X-Forwarded-For #if using npm as proxy
```
# **Disclaimer**
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
