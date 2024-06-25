FROM node:lts-bullseye

# File Author / Maintainer
LABEL org.opencontainers.image.authors="AntzCode Ltd <www.antzcode.com>"

EXPOSE 3003

# Let it install without stopping for user input
ARG DEBIAN_FRONTEND=noninteractive

# Update the repository sources list
RUN apt-get update

WORKDIR /usr/src/app

# Include server admin tools
RUN apt-get install -y nano htop ncdu git curl

RUN yarn set version stable
RUN npm i -g @nestjs/cli
RUN npm i -g @nestjs/common
RUN npm i -g @nestjs/core
RUN npm i -g pkg

WORKDIR /home/node/app

# RUN mkdir -p /usr/src/app
COPY ./install/* /home/node/app

RUN yarn install

CMD ["yarn", "dev"]
