FROM node:8.11.4-alpine

LABEL maintainer="Ian Klek"

RUN mkdir -p /app

WORKDIR /app
#
COPY package.json .
##
RUN ["npm", "install", "-g", "yarn"]
RUN ["yarn", "install"]
##
COPY . /app
##
EXPOSE 4000/tcp
#
ENTRYPOINT ["node", "src/index.js"]
