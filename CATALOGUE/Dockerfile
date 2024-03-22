# Use the official node image as the base image
FROM node:14

WORKDIR /opt/server

ENV INSTANA_AUTO_PROFILE true

COPY package.json .

COPY server.js .

RUN npm install

ENV  MONGO=true

CMD ["node", "server.js"]

