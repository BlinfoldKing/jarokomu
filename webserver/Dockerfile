FROM node:alpine

RUN apk update && \
    apk add ca-certificates openssl && \
    update-ca-certificates

WORKDIR /client
COPY . .

RUN npm install
RUN npm build

CMD [ "npm", "start" ]
