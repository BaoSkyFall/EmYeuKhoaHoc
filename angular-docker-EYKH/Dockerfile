# Stage 1
FROM node:latest
RUN npm install
COPY . ./
RUN npm run build
# Stage 2
FROM nginx:1.17.1-alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY dist/angular-docker-EYKH /usr/share/nginx/html
