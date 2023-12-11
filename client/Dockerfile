FROM node:21.4.0-alpine3.18

# increase heapsize for javascript
ENV NODE_OPTIONS=--max-old-space-size=16384
ENV GENERATE_SOURCEMAP=false

COPY package*.json ./

RUN npm install

ADD . .

RUN npm run build