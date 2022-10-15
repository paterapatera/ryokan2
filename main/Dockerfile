FROM node:latest

RUN curl -f https://get.pnpm.io/v6.16.js | node - add --global pnpm

COPY pnpm-lock.yaml ./

RUN pnpm fetch


ADD . ./
RUN pnpm install -r --offline


EXPOSE 3000
CMD [ "npx", "next", "dev" ]
