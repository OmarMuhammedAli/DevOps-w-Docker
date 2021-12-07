# Build an image for a golang project
FROM ubuntu:latest

WORKDIR /usr/src/app

COPY . .

RUN apt-get update && apt-get install -y curl gcc
RUN curl -O https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz
RUN tar -xvf go1.16.linux-amd64.tar.gz
RUN mv go /usr/local

ENV GOPATH=$HOME/WORKDIR
ENV PATH=$PATH:/usr/local/go/bin:$GOPATH/bin

RUN go build

RUN go test ./...

ENV PORT=8080
ENV REQUEST_ORIGIN="http://localhost:8080"

CMD ./server

EXPOSE 8080