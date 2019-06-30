FROM ubuntu:16.04

ENV LC_ALL=C.UTF-8

RUN apt-get update && apt-get install -y wget apt-utils python3 python3-pip ffmpeg && \
    pip3 install --user --upgrade yle-dl && \
    cp /root/.local/bin/yle-dl /usr/local/bin/ && \
    chmod a+x /usr/local/bin/yle-dl

WORKDIR /yle-dl

ENTRYPOINT ["yle-dl"]