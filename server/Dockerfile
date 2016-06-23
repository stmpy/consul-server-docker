FROM consul:v0.6.4

ENV DOCKER_VERSION 1.11.0

RUN apk --no-cache add \
    curl

RUN curl -o /tmp/docker.tgz "https://get.docker.com/builds/Linux/x86_64/docker-$DOCKER_VERSION.tgz" \
  && tar -xvzf /tmp/docker.tgz \
  && rm /tmp/docker.tgz \
  && mv docker/* /usr/local/bin/

RUN addgroup -g 999 docker \
  && adduser consul docker
