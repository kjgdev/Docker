FROM node:alpine
WORKDIR /app
COPY package.json ./
COPY package-lock.json ./

COPY ./ ./
RUN apk add --update python make g++\
   && rm -rf /var/cache/apk/*
RUN npm i
CMD ["npm", "run", "start"]