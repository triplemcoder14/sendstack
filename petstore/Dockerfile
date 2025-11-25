FROM node:22-slim
WORKDIR /src/app
MAINTAINER Muutassim
RUN npm config set fetch-retries 5 \
    && npm config set fetch-retry-mintimeout 20000 \
    && npm config set fetch-retry-maxtimeout 120000 \
    && npm config set fetch-timeout 300000 \
    && npm config set registry https://registry.npmjs.org/
COPY package.json package-lock.json* ./
RUN npm install --legacy-peer-deps
ENV NODE_ENV=development
RUN npm install --legacy-peer-deps
COPY . .

CMD ["npm", "run", "start:dev"]
