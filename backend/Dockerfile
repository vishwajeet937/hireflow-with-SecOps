FROM node:22-alpine3.22

WORKDIR /app

RUN apk update && apk upgrade \
    && npm install -g npm@11 \
    && npm cache clean --force

COPY package*.json ./

RUN npm install \
    && npm cache clean --force

COPY . .

EXPOSE 3000

CMD ["npm", "start"]