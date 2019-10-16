FROM debian:stretch-slim

LABEL maintainer="Ivan D Barron <ivandavid77@gmail.com>"

ENV LANG C.UTF-8

RUN apt-get update && \
    apt-get -y install wget gnupg2 && \
    wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && \
    dpkg -i erlang-solutions_1.0_all.deb && \
    apt-get update && \
    apt-get -y install esl-erlang && \
    apt-get clean