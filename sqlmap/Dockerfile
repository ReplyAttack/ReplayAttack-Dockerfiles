FROM ubuntu:18.04

MAINTAINER Austin Songer (austin@songer.pro)

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update; apt-get -y dist-upgrade;apt-get -y install sqlmap; rm -rf /var/lib/apt/lists/*

ENTRYPOINT sqlmap $@