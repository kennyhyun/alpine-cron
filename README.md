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

![Screenshot](https://raw.githubusercontent.com/kennyhyun/alpine-cron/master/alpine.cron.png)

## Tips

Set your timezone using TZ

`.env`
```
TZ=Australia/Sydney
```
