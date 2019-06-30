FROM node:alpine

WORKDIR /backend

RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh && \
    git clone https://github.com/docker-hy/backend-example-docker.git /backend && \
    npm install

ENV FRONT_URL http://localhost:5000
EXPOSE 8000

CMD ["npm", "start"]