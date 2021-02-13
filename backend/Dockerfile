FROM node:lts-alpine
WORKDIR /usr/app/
RUN apk add git
RUN git clone https://github.com/eosdg/server.git .
RUN npm install
RUN npm run build

EXPOSE 3420
CMD [ "npm", "start" ]
