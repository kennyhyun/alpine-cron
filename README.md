# alpine-cron
A cron container with Alpine Linux only takes 5MB

## Goal

- Small image size
- Logging to docker without using file logs

## Packages added

Using dcron(dillon's cron daemon) instead of busybox's

- dcron
- tzdata
- bash
- curl

## Check working in your local environment

```
$ docker-compose up
```
