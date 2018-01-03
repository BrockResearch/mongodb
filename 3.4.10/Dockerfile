# Version: 1.0.0
FROM alpine:3.7
MAINTAINER Brock Research 

RUN apk add --no-cache \
    ca-certificates

RUN apk update

RUN apk add mongodb=3.4.10-r0

RUN mkdir -p /data/db /data/configdb
RUN chown -R mongodb:mongodb /data/db /data/configdb

COPY etc/conf.d/mongodb /etc/conf.d/mongodb

EXPOSE 27017
CMD ["mongod"]
