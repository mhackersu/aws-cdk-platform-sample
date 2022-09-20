FROM node:16 as builder
WORKDIR /usr/src/app/producer/api
COPY package.json ./
RUN npm install
COPY *.ts ./
RUN npm run build-api
    
FROM node:16
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app/producer/api/dist/* ./
CMD [ "node", "express.js" ]