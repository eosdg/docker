FROM node:lts-alpine
WORKDIR /usr/app/
COPY source/package*.json ./
RUN npm ci --silent
COPY source .
RUN npm run build

EXPOSE 3420
CMD [ "npm", "start" ]
