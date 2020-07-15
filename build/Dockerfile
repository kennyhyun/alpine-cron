FROM alpine:3.12.0
 
RUN apk update && apk add dcron tzdata bash curl && rm -rf /var/cache/apk/*

RUN mkdir -m 0644 -p /var/spool/cron/crontabs && mkdir -m 0644 -p /etc/cron.d

COPY /entry /
COPY /startup /
COPY /logger /

ENTRYPOINT ["/entry"]
CMD ["/startup"]
