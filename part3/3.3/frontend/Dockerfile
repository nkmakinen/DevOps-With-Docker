FROM ubuntu:16.04

WORKDIR /frontend-app

RUN apt-get update && apt-get install -y wget curl npm apt-utils git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend-app && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown app:app /frontend-app

USER app

RUN npm install

ENV API_URL http://localhost:8000
EXPOSE 5000

CMD ["npm", "start"]