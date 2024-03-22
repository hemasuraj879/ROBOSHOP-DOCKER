# Use an official Node.js image as the base image
FROM node:14

# Expose this application on port
EXPOSE 8080

RUN groupadd -r cart && useradd -r -g cart cart


# Set the working directory in the container
WORKDIR /app

RUN chown -R cart:cart /opt/app
USER cart

# Setting up Environment variables
ENV CATALOGUE_PORT=8080

# Copy package.json and  to the container
COPY package.json .

# Copy server.js and  to the container
COPY server.js .

# Install dependencies
RUN npm install

# Define the command to run your Node.js application
CMD ["node", "server.js"]

