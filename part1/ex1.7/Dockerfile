FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl wget dos2unix
COPY start.sh .
RUN dos2unix start.sh
CMD ["./start.sh"]