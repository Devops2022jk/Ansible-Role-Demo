FROM ubuntu:20.04
MAINTAINER Kubendran
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y \
    software-properties-common \
    python3 \
    python3-pip \
    curl && \
    rm -rf /var/lib/apt/lists/*
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash - && \
    apt-get install -y nodejs && \
    rm -rf /var/lib/apt/lists/
RUN mkdir -p /var/www
ADD app.js /var/www/app.js
CMD ["node", "/var/www/app.js"]
