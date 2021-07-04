FROM nginx:latest

RUN apt-get update && apt-get install -y \
    vim \
    nano

RUN rm /etc/nginx/conf.d/*
ADD default.conf /etc/nginx/conf.d/