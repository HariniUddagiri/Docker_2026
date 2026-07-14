#FROM node:20
FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense 
#for alpine commands are little different
RUN mkdir /opt/backend 
RUN chown -R expense:expense /opt/backend
 #chamging the ownership of the directory to the user expense
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
USER expense 
#to makesure container runs with non root user
CMD ["node", "index.js"]