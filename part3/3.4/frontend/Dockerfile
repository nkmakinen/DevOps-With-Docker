FROM node:alpine

WORKDIR /frontend-app

RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend-app && \
    npm install

ENV API_URL http://localhost:8000
EXPOSE 5000

CMD ["npm", "start"]