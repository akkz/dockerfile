FROM       ubuntu:14.04
MAINTAINER Akkz

RUN apt-get update \
    && apt-get install python-pip \
    && pip install shadowsocks 
   
ENV SERVER_ADDR 0.0.0.0
ENV SERVER_PORT 80
ENV LOCAL_ADDR  0.0.0.0
ENV LOCAL_PORT  7080
ENV PASSWORD    password
ENV METHOD      aes-256-cfb
ENV TIMEOUT     600
ENV DNS_ADDR    8.8.8.8

EXPOSE 7080

CMD ss-server -s $SERVER_ADDR \
              -p $SERVER_PORT \
			  -b $LOCAL_ADDR \
			  -l $LOCAL_PORT \
              -k $PASSWORD \
              -m $METHOD \
              -t $TIMEOUT