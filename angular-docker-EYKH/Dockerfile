# NPM
# Stage 1
FROM node:latest as build-image
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

# Stage 2
FROM nginx:1.17.1-alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build-image /app/dist/angular-docker-EYKH /usr/share/nginx/html



# Yarn
# Stage 1
# FROM node:latest as build-app
# WORKDIR /app
# RUN npm -g yarn
# RUN npm i gzipper -g
# COPY . .
# RUN yarn
# RUN yarn deployUser


# # Stage 2
# FROM nginx:1.17.1-alpine
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY --from=build-app /app/localSourceMaps /usr/share/nginx/html