FROM node:lts-alpine
RUN groupadd -r app && useradd -r -g app app
USER app
WORKDIR /usr/app/
RUN apk add git
RUN git clone https://github.com/eosdg/server.git .
RUN npm install
RUN npm run build

EXPOSE 3420
CMD [ "npm", "start" ]
