FROM alpine:3.18.2

MAINTAINER ariskourt

ARG USER=ssh
ENV HOME /home/$USER
ENV GROUP ssh

RUN apk update && apk add --no-cache \
    openssh-client \
    ca-certificates \
    bash \
    curl

RUN addgroup -g 1001 $GROUP
RUN adduser -S --ingroup $GROUP --uid 1001 $USER

WORKDIR $HOME
USER $USER
