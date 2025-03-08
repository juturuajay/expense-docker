#FROM node:20
# IC - 1
FROM node:20.18.3-alpine3.21
# on top of IC -1 instruction 2 is executes and save this layes as 2 image IC-1 remved
RUN addgroup -S expense && adduser -S expense -G expense && \
 mkdir /opt/backend && \
 chown -R expense:expense /opt/backend
WORKDIR /opt/backend
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
COPY package.json .
COPY *.js ./
RUN npm install 
CMD ["node", "index.js"]
