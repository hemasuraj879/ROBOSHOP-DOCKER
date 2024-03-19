FROM nginx:latest

RUN rm -rf  /usr/share/nginx/html/*

ADD Static /usr/share/nginx/html

COPY roboshop.conf /etc/nginx/conf.d/

