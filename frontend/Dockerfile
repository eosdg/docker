# build stage
FROM node:lts-alpine as build-stage
WORKDIR /usr/app/
COPY source/package*.json ./
COPY source/config.template.js ./
RUN npm ci --silent
COPY source .
RUN npm run build

# production stage
FROM nginx:stable-alpine as production-stage
COPY --from=build-stage /usr/app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
