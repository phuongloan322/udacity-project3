## Build
FROM beevelop/ionic:latest AS ionic

## Create app directory
WORKDIR /usr/src/app

## Install dependencies
COPY package*.json ./

RUN npm ci

## Bundle app source
COPY . .

RUN ionic build

## Run
FROM nginx:alpine

## COPY www /usr/share/nginx/html
COPY --from=ionic /usr/src/app/www /usr/share/nginx/html
