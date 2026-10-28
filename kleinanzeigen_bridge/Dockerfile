# Multi-arch manifest (amd64 + arm64): buildx picks the matching image.
# Pinned by digest (upstream only publishes moving `latest`/`preview` tags):
# the bridge parses the bot's CLI output, so a silent bot update on rebuild
# could break it without any version change here. This digest is `latest`
# as of 2026-10-28 (release of 2026-10-24); bump it deliberately.
FROM ghcr.io/second-hand-friends/kleinanzeigen-bot@sha256:07d4032e4f35e16d03399d0035a358bb498b690f11775f1240041d3263ddca1c

# Supervisor passes the add-on version from config.yaml as BUILD_VERSION.
ARG BUILD_VERSION
ENV BRIDGE_VERSION=${BUILD_VERSION}

# The base image is the official kleinanzeigen-bot image: Debian trixie with
# Chromium, KasmVNC, openbox and the compiled bot at /opt/kleinanzeigen-bot.
# The bridge only needs Python with aiohttp and PyYAML from Debian, and tini
# to reap Chromium's child processes (add-on runs with init: false).
USER root
RUN apt-get update \
 && apt-get install --no-install-recommends -y python3 python3-aiohttp python3-yaml tini \
 && rm -rf /var/lib/apt/lists/*

COPY app/ /opt/bridge/

ENTRYPOINT ["/usr/bin/tini", "--"]
CMD ["/bin/bash", "/opt/bridge/start.sh"]
