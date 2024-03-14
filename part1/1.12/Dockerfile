FROM ubuntu:latest

EXPOSE 5000

WORKDIR usr/src/app

RUN apt-get update && apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt-get install -y sudo
RUN sudo apt install -y nodejs

COPY ./example-frontend/package-lock.json .
COPY ./example-frontend/package.json .

RUN npm install

COPY ./example-frontend/ .

RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
