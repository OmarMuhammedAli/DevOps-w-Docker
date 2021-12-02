FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY scrapper.sh .

RUN chmod +x scrapper.sh

RUN apt-get update; apt-get install curl -y

CMD ./scrapper.sh