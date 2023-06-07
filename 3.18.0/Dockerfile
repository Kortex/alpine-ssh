FROM alpine:3.18.0

ARG USER=ssh
ENV HOME /home/$USER

RUN apk add --update sudo

RUN adduser -D $USER \
        && echo "$USER ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/$USER \
        && chmod 0440 /etc/sudoers.d/$USER

RUN apk add --no-cache \
      openssh-client \
      ca-certificates \
      bash

USER $USER
WORKDIR $HOME