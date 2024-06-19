ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on

RUN \
    apk add --no-cache ddclient --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing

RUN \
    apk add --no-cache openrc

# Copy data for add-on
COPY rootfs /

# ports and volumes
VOLUME /data
