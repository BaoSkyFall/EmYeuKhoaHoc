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

# docker build -t <name-image> .
# docker run --name <name-container> -d -p 8080:80 <name-image>
# docker save -o C:\Users\baoppq\Desktop\EmYeuKhoaHoc\file.tar <name-image>

# docker run -d -p 80:80 <docker-img-path-file>
# docker load -i <path to image tar file>
