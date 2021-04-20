# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.166.1/containers/alpine/.devcontainer/base.Dockerfile

# [Choice] Alpine version: 3.13, 3.12, 3.11, 3.10
ARG VARIANT="3.13"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-alpine-${VARIANT}

# Add alpine v3.6 main repo to get mongo db
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/main' >> /etc/apk/repositories
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/community' >> /etc/apk/repositories

RUN apk update \
    && apk add --no-cache \
    nodejs \
    npm \
    python3 \
    py3-pip \
    mongodb=3.4.4-r0

RUN npm install -g bower
RUN npm install -g gulp-cli
RUN npm install -g nodemon