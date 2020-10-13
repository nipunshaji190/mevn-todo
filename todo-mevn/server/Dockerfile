FROM ubuntu:18.04

RUN apt update

RUN apt-get -y install curl gnupg

RUN curl -sL https://deb.nodesource.com/setup_14.x  | bash -

RUN apt-get -y install nodejs && node -v && npm -v 

WORKDIR /app

COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 9000
CMD [ "node", "server.js"]
