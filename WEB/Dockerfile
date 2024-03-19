FROM nginx:latest

RUN rm -rf /usr/share/nginx/html/*

RUN rm -rf /etc/nginx/nginx.conf

RUN rm -rf /etc/nginx/conf.d/default.conf

COPY roboshop.conf /etc/nginx/nginx.conf

COPY Static /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]