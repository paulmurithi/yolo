# use multistage builds to reduce image size
# Stage 1: Build the application
FROM node:16.20.1-alpine3.17 AS build

# set working directory
WORKDIR /client

# install app dependencies
#copies package.json and package-lock.json to Docker environment
COPY package.json ./
COPY package-lock.json ./

# Installs all node packages
RUN npm install 

# Copies everything over to Docker environment
COPY . ./
RUN npm run build

#Stage 2
#pull the official nginx:1.25.1-alpine base image
FROM nginx:1.25.1-alpine

#copies code to the container directory
# Set working directory to nginx resources directory
WORKDIR /usr/share/nginx/html

# Remove default nginx static resources
RUN rm -rf ./*

# Copies static resources from builder stage
COPY --from=build /client/build .

# Containers run nginx with global directives and daemon off
ENTRYPOINT ["nginx", "-g", "daemon off;"]
