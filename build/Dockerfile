FROM alpine:latest
 
RUN apk update && apk add dcron tzdata docker-cli bash curl && rm -rf /var/cache/apk/*

RUN mkdir -m 0644 -p /var/spool/cron/crontabs && mkdir -m 0644 -p /etc/cron.d

COPY /entry /
COPY /startup /
COPY /logger /

ENTRYPOINT ["/entry"]
CMD ["/startup"]
