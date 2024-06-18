ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on

RUN \
    apk add --no-cache ddclient

# Copy data for add-on
COPY rootfs /

# ports and volumes
VOLUME /data
