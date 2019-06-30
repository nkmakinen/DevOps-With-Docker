FROM node:10

WORKDIR /frontend-app

RUN apt-get update && apt-get -y install git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend-app && \
    npm install

ENV API_URL http://localhost:8000
EXPOSE 5000

CMD ["npm", "run", "build"]