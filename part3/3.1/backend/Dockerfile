FROM ubuntu:16.04

RUN apt-get update && apt-get install -y wget curl npm apt-utils git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/backend-example-docker.git /backend && \
    npm install && \
    apt-get purge -y --auto-remove curl && \ 
    rm -rf /var/lib/apt/lists/* 

WORKDIR /backend
ENV FRONT_URL http://localhost:5000
EXPOSE 8000

CMD ["npm", "start"]