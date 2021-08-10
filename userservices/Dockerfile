FROM node:14.15.0-alpine3.10 

WORKDIR /usr/share/app

COPY userservices/server.js server.js
COPY node_modules node_modules

EXPOSE 4015

CMD ["node", "server.js"]