FROM ubuntu:18.04

MAINTAINER Austin Songer (austin@songer.pro)

ENV DEBIAN_FRONTEND noninteractive

ENV LANG=en_US.UTF-8

RUN apt-get update && apt-get install -y \
	ca-certificates \
	curl \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

RUN groupadd -r mitmproxy && useradd -r -g mitmproxy mitmproxy \
    && mkdir -p /home/mitmproxy/.mitmproxy \
	&& chown -R mitmproxy:mitmproxy /home/mitmproxy

ENV MITMPROXY_VERSION 5.1.1
RUN curl -sSL "https://snapshots.mitmproxy.org/${MITMPROXY_VERSION}/mitmproxy-${MITMPROXY_VERSION}-linux.tar.gz" | tar -vxzC /usr/local/bin

VOLUME /home/mitmproxy/.mitmproxy

COPY docker-entrypoint.sh /usr/local/bin/

EXPOSE 8080 8081

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["mitmproxy"]