# base image
FROM node:12.2.0-alpine

# set working directory
WORKDIR /usr/src/app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /usr/src/app/node_modules/.bin:$PATH

# install and cache app dependencies
COPY package.json /usr/src/app/package.json
RUN npm install
RUN npm install react-scripts@3.3.0 -g

# start app
CMD ["npm", "start"]