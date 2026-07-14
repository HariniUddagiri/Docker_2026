#FROM node:20
FROM node:20.18.3-alpine3.21 AS builder
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
RUN npm install

FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense && \
#for alpine commands are little different
     mkdir /opt/backend && \
     chown -R expense:expense /opt/backend
      #combining the commands to reduce the number of layers in the image
ENV DB_HOST="mysql"
WORKDIR /opt/backend
USER expense 
COPY --from=builder /opt/backend/ /opt/backend/
#to makesure container runs with non root user
CMD ["node", "index.js"]