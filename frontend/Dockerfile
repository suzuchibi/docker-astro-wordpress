# https://hub.docker.com/_/node
FROM node:20.18-alpine3.19

ENV TZ=Asia/Tokyo
ENV NPM_VERSION=10.9.0

RUN apk update && \
    apk upgrade && \
    npm install -g npm@${NPM_VERSION}

WORKDIR /app
COPY ./astro .
ENV HOST 0.0.0.0
ENV PORT=4321
EXPOSE 4321