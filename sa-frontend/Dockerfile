FROM node:lts-alpine AS build

WORKDIR /src
COPY . ./

RUN npm install
RUN npm run build

FROM nginx:alpine

COPY --from=build /src/build /usr/share/nginx/html
