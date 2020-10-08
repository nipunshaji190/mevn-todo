FROM ubuntu:18.04

RUN apt update

RUN apt-get -y install curl gnupg

RUN curl -sL https://deb.nodesource.com/setup_14.x  | bash -

RUN apt-get -y install nodejs

RUN node -v

RUN npm -v

WORKDIR /app

COPY package*.json ./

COPY . .

VOLUME /app/node_modules
VOLUME ./server:/app
EXPOSE 9000
CMD [ "bash", "-c", "npm install && npm run serve" ]
