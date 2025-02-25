ARG BUILD_FROM=ghcr.io/home-assistant/aarch64-base:latest
FROM $BUILD_FROM

ENV LANG C.UTF-8
RUN apk add --no-cache ffmpeg curl bash

# Install MediaMTX
RUN curl -L -o /usr/local/bin/mediamtx https://github.com/bluenviron/mediamtx/releases/latest/download/mediamtx_linux_arm64v8 \
    && chmod +x /usr/local/bin/mediamtx

# Copy run script
COPY run.sh /run.sh
RUN chmod +x /run.sh

CMD [ "/run.sh" ]