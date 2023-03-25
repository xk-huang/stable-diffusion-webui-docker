FROM bash:alpine3.15

ENV http_proxy 'http://10.81.2.101:9910'
ENV https_proxy 'http://10.81.2.101:9910'
RUN wget cip.cc

RUN apk add parallel aria2
COPY . /docker
RUN chmod +x /docker/download.sh
ENTRYPOINT ["/docker/download.sh"]
