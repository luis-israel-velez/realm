FROM node:14.15.0-alpine3.10 

WORKDIR /usr/share/app

COPY app/server.js server.js
COPY node_modules node_modules

EXPOSE 3015

CMD ["node", "server.js"]