FROM node:lts-alpine
WORKDIR /usr/app/
COPY server-source/package*.json ./
RUN npm ci --silent
COPY server-source .
RUN npm run build

EXPOSE 3420
CMD [ "npm", "start" ]
