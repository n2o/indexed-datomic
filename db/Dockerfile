FROM java:8-alpine

RUN apk add --no-cache bash

COPY datomic /datomic
WORKDIR /datomic

EXPOSE 8998
CMD bin/run -m datomic.peer-server -h localhost -p 8998 -a $DATOMIC_ACCESS_KEY,$DATOMIC_SECRET -d $DATOMIC_DB_NAME,datomic:mem://$DATOMIC_DB_NAME
