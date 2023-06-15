FROM debian:stable-slim

RUN apt-get update \
    && apt-get install -y ssh

RUN mkdir -p $HOME/.ssh \
    && chmod 700 $HOME/.ssh

RUN touch $HOME/.ssh/known_hosts \
    && chown $USER $HOME/.ssh/known_hosts