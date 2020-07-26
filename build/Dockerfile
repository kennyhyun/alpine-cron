FROM alpine:latest
 
RUN apk update && apk add dcron tzdata docker-cli bash curl && rm -rf /var/cache/apk/*

RUN mkdir -m 0644 -p /etc/cron.d
RUN rm -rf /var/spool/cron/crontabs && mkdir -m 0666 -p /var/spool/cron/crontabs

COPY /entrypoint /entrypoint.cron
COPY /startup /startup.cron
COPY /logger /

ENTRYPOINT ["/entrypoint.cron"]
CMD ["/startup.cron"]
