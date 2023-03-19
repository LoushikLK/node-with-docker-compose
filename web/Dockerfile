# syntax=docker/dockerfile:1

FROM node:16.15.1

ENV NODE_ENV=production

WORKDIR /

COPY ["package.json", "yarn.lock*", "./"]

RUN yarn --production=true

COPY . .

RUN yarn build

EXPOSE 3000

CMD [ "yarn", "start" ]

