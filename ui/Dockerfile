FROM node:14.21.3-alpine as node-builder

WORKDIR /app

 #Install app dependencies
COPY package.json .
RUN npm install

 #Bundle app source
COPY . .

RUN npm run build

#FROM nginx:stable-alpine

#WORKDIR /usr/share/nginx/html

#COPY --from=node-builder /app/dist .
#EXPOSE 8080


FROM nginx:stable-alpine
WORKDIR /app
COPY ./dist .
COPY ./nginx.conf /etc/nginx/nginx.conf 
RUN command


