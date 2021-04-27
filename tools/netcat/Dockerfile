FROM ubuntu:18.04

MAINTAINER Austin Songer (austin@songer.pro)

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y \
	netcat \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "netcat" ]