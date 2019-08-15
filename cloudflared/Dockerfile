FROM alpine:latest

LABEL maintainer="Fred Gauthier <fred.gauthier.dev@gmail.com>" \
    Description="A Cloudflared container, build with Alpine"

ARG  ARCHITECTURE
ENV  ARCHITECTURE $ARCHITECTURE

ARG  PORT
ENV  PORT $PORT

RUN apk update \
    && printenv \
    && echo "test ${ARCHITECTURE}" \
    && echo "test https://bin.equinox.io/c/VdrWdbjqyF/cloudflared-stable-linux-${ARCHITECTURE}.tgz" \
    && apk add --no-cache --virtual install-dependencies curl tar\
    && curl -fSL "https://bin.equinox.io/c/VdrWdbjqyF/cloudflared-stable-linux-${ARCHITECTURE}.tgz" | tar xzC /usr/local/bin \
    # Clean up
    && apk del --purge install-dependencies \
    && rm -rf /var/cache/apk/*

EXPOSE $PORT