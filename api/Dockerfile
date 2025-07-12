# Use a Node.js 20 LTS base image
FROM node:20-slim

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package*.json ./
RUN npm install --production

# Bundle app source
COPY . .

# Cloud Run services listen on the port defined by the PORT environment variable (default 8080)
EXPOSE 8080

# Run the web server using the 'start' script defined in package.json
CMD [ "npm", "start" ]