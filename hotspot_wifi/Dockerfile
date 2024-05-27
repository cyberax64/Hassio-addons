ARG BUILD_FROM
# hadolint ignore=DL3006
FROM ${BUILD_FROM}

# Set shell
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt-get update
RUN apt-get install -y software-properties-common 
RUN add-apt-repository ppa:ondrej/php
RUN apt-get install -y iptables iproute2 iw net-tools hostapd dnsmasq

COPY /rootfs / 

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="hotspot_wifi" \
    io.hass.description="hotspot_wifi" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="elodie Elizalde <cyberax@protonmail.com>" \
    org.label-schema.description="hotspot_wifi" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="hotspot_wifi" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://github.com/cyberax64/Hassio-addons/" \
    org.label-schema.usage="https://github.com/cyberax64/Hassio-addons/tree/master/hotspot_wifi/tree/master/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/cyberax64/Hassio-addons/tree/master/hotspot_wifi" \
    org.label-schema.vendor="elodie Elizalde"

