FROM node:22-slim
MAINTAINER Muutassim
RUN mkdir -p /src/app
WORKDIR /src/app
COPY package.json package-lock.json* ./
RUN npm install --legacy-peer-deps
COPY . .
CMD ["npm", "start"]
