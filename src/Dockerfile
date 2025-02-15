FROM ubuntu
WORKDIR /app

RUN useradd app
ARG NODE_MAJOR=20

RUN apt update \
    && apt install -y curl \
    && curl -fsSL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh \
    && bash nodesource_setup.sh \
    && apt install -y nodejs \
    && apt clean

COPY . .

RUN npm install

EXPOSE 8080

ENTRYPOINT ["node", "server.js"]
