# Use the official mongo image as the base image
FROM mongo:5

COPY *.js /docker-entrypoint-initdb.d/

COPY mongo.conf /etc/mongod.conf

