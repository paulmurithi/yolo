# use multistage builds to reduce image size
# Stage 1: Build the application
FROM node:16.20.1-alpine3.17 AS build

# set working directory
WORKDIR /client

#copies package.json and package-lock.json to Docker environment
COPY package*.json ./

# Installs all node packages
RUN npm install 

# Copies everything over to Docker environment
COPY . ./

ENTRYPOINT [ "npm", "start" ]

