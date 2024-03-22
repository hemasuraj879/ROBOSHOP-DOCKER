# Use an official Node.js image as the base image
FROM node

# Set the working directory in the container
WORKDIR /app

# Setting up Environment variable
ENV MONGO=true

# Copy package.json and  to the container
COPY package.json .

# Copy server.js and  to the container
COPY server.js .

# Install dependencies
RUN npm install

# Define the command to run your Node.js application
CMD ["node", "server.js"]