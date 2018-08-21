FROM node:8.11.3-alpine

RUN mkdir -p /app

WORKDIR /app

COPY package.json .

RUN ["npm", "install"]

COPY . /app

EXPOSE 4200/tcp

ENTRYPOINT ["npm", "start", "--", "--host", "0.0.0.0", "--poll", "500"]
