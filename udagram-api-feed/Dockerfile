FROM node:14-alpine

## create app directory
WORKDIR /usr/src/app

## Install all dependencies
COPY package*.json ./

RUN npm ci

## Bundle app source
COPY . .

EXPOSE 8080

CMD ["npm", "run", "prod"]
