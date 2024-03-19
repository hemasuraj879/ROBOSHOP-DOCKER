FROM nginx:latest

RUN /usr/share/nginx/html/*

ADD https://roboshop-builds.s3.amazonaws.com/web.zip /usr/share/nginx/html

COPY roboshop.conf /etc/nginx/conf.d/

