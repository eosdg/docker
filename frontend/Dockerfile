# build stage
FROM node:lts-alpine as build-stage
WORKDIR /usr/app/
RUN apk add git
RUN git clone https://github.com/eosdg/client.git .
RUN npm install
RUN npm run build

# production stage
FROM nginx:stable-alpine as production-stage
COPY --from=build-stage /usr/app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]