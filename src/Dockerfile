FROM node:20.9.0

WORKDIR /app

COPY . .

RUN npm install

EXPOSE 8080

ENTRYPOINT ["node", "server.js"]
