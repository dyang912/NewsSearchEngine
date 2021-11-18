FROM node:latest

LABEL org.opencontainers.image.source="https://github.com/dyang912/NewsSearchEngine"

WORKDIR /app
COPY package.json ./
COPY package-lock.json ./
RUN npm install
COPY . ./
CMD ["npm", "start"]

