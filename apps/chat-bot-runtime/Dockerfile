FROM node:22-alpine AS build
WORKDIR /app

COPY package.json package-lock.json ./
COPY modbots-backend/package.json ./modbots-backend/package.json
COPY apps/chat-bot-runtime/package.json ./apps/chat-bot-runtime/package.json
RUN npm ci

COPY apps/chat-bot-runtime ./apps/chat-bot-runtime
RUN npm run build --workspace apps/chat-bot-runtime

FROM node:22-alpine AS runtime
WORKDIR /app
ENV NODE_ENV=production

COPY --from=build /app/apps/chat-bot-runtime/dist ./dist

CMD ["node", "dist/index.js"]
