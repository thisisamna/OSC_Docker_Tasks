FROM node

WORKDIR /app

RUN npm install

COPY package*.json /app
COPY src /app


CMD ["node", "app.js"]