FROM node:7.7-alpine

# install deps
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy deps
RUN mkdir -p /opt/coffeepedia-app && cp -a /tmp/node_modules /opt/coffeepedia-app

# Setup workdir
WORKDIR /opt/coffeepedia-app
COPY . /opt/coffeepedia-app

# run
EXPOSE 3000
CMD ["npm", "start"]