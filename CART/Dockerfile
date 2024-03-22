# Use an official Node.js image as the base image
FROM node:14

# Expose this application on port
EXPOSE 8080

# Set the working directory in the container
WORKDIR /app

# Setting up Environment variables
ENV INSTANA_AUTO_PROFILE true
ENV CATALOGUE_PORT=8080

# Copy package.json and  to the container
COPY package.json .

# Copy server.js and  to the container
COPY server.js .

# Install dependencies
RUN npm install

# Define the command to run your Node.js application
CMD ["node", "server.js"]

