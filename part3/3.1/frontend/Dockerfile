FROM ubuntu:16.04

RUN apt-get update && apt-get install -y wget curl npm apt-utils git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend-app && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /frontend-app
ENV API_URL http://localhost:8000
EXPOSE 5000

CMD ["npm", "start"]