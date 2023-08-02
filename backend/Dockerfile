
FROM node:18-alpine

RUN apk update && apk add

WORKDIR /app

COPY dist dist
COPY package.json .
COPY package-lock.json .

RUN npm ci --only=production

EXPOSE 3000
CMD [ "node", "dist/server.js" ]