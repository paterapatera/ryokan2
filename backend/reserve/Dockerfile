FROM node:latest

RUN curl -f https://get.pnpm.io/v6.16.js | node - add --global pnpm

WORKDIR /app/backend/reserve

RUN pnpm config set store-dir /app/.pnpm-store
COPY pnpm-lock.yaml .
RUN pnpm fetch
COPY package.json .
RUN pnpm install -r --offline

EXPOSE 3000
CMD ["npx", "start:prod"]
