#!/bin/bash

FROM ubuntu:latest

WORKDIR /usr/src/app

# COPY the application source code into the container at /usr/src/app
COPY . .

# Expose port 5000 for the frontend service
EXPOSE 5000

# Install curl
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y nodejs

# Install node_modules
RUN npm install

# Build the static files
RUN npm run build

# install npm package serve to serve the project
RUN npm install -g serve

# Use serve to serve the static files
CMD ["serve", "-s","-l","5000","build"]