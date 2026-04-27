FROM node:20-alpine

WORKDIR /usr/src/app

COPY backend/package*.json ./
COPY backend/prisma ./prisma

RUN npm install
RUN npx prisma generate

COPY backend/ .

ENV NODE_ENV=production
EXPOSE 3000

CMD ["node", "src/server.js"]
