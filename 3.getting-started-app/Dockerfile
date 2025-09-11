# syntax=docker/dockerfile:1

FROM node:lts-alpine
WORKDIR /app
COPY package.json .
RUN yarn install --production
COPY . .
COPY healthcheck.sh .
RUN chmod +x healthcheck.sh
CMD ["node", "src/index.js"]
EXPOSE 3000