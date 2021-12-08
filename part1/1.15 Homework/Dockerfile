FROM ubuntu:latest

WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y \
curl \
python3.8 \
python3-pip 

RUN pip3 install mapillary

CMD ["python3"]