# use multistage builds to reduce image size
FROM node:16.20.1-alpine3.17

# set working directory
WORKDIR /backend

# install app dependencies
#copies package.json and package-lock.json to Docker environment
COPY package*.json ./

# Installs all node packages
RUN npm install 

# Copies everything over to Docker environment
COPY . ./
ENTRYPOINT ["npm", "start"]
