ARG BUILD_FROM
FROM $BUILD_FROM

ARG S6_OVERLAY_VERSION=3.2.0.0

# Install requirements for add-on

# RUN \
#     apk add --no-cache openrc

RUN \
    apk add --no-cache ddclient --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing

# Copy data for add-on
COPY rootfs /

ADD https://github.com/just-containers/s6-overlay/releases/download/v${S6_OVERLAY_VERSION}/s6-overlay-noarch.tar.xz /tmp
RUN tar -C / -Jxpf /tmp/s6-overlay-noarch.tar.xz
ADD https://github.com/just-containers/s6-overlay/releases/download/v${S6_OVERLAY_VERSION}/s6-overlay-x86_64.tar.xz /tmp
RUN tar -C / -Jxpf /tmp/s6-overlay-x86_64.tar.xz
ADD https://github.com/just-containers/s6-overlay/releases/download/v${S6_OVERLAY_VERSION}/syslogd-overlay-noarch.tar.xz /tmp
RUN tar -C / -Jxpf /tmp/syslogd-overlay-noarch.tar.xz


ENTRYPOINT ["/init"]
