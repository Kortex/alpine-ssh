FROM alpine:3.18

MAINTAINER ariskourt

ARG USER_NAME=ssh
ARG USER_GROUP=ssh

ARG USER_HOME=/home/$USER_NAME

RUN apk update && apk add --no-cache \
    openssh-client \
    ca-certificates \
    bash \
    curl \
    rsync

RUN addgroup -g 1001 $USER_GROUP
RUN adduser -S --ingroup $USER_GROUP --uid 1001 $USER_NAME

WORKDIR $USER_HOME
USER $USER_NAME
