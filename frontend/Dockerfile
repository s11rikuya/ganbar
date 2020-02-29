FROM node:12.16.1

ENV HOME="/app" \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo

WORKDIR /ganbar/frontend
COPY package*.json ./

RUN apt update && \
    apt upgrade && \
    npm install -g npm && \
    npm install -g @vue/cli

ENV HOST 0.0.0.0
EXPOSE 3000
