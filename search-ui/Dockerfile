FROM node:latest

LABEL org.opencontainers.image.source="https://github.com/dyang912/NewsSearchEngine"

WORKDIR /app

RUN export NODE_OPTIONS=--openssl-legacy-provider && yarn build && yarn install --production --ignore-scripts --prefer-offline

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

COPY package.json ./
COPY package-lock.json ./
RUN npm install
COPY . ./

CMD ["npm", "start"]

