FROM mhart/alpine-node:16 as base

WORKDIR /usr/src/app

FROM base as deps

COPY package*.json ./

RUN npm ci --only=production

FROM base as build

COPY . .

COPY --from=deps /usr/src/app/node_modules ./node_modules

ARG REACT_APP_BACKEND_URL
ENV REACT_APP_BACKEND_URL=${REACT_APP_BACKEND_URL}
RUN REACT_APP_BACKEND_URL=${REACT_APP_BACKEND_URL} npm run build

FROM mhart/alpine-node:16

WORKDIR /usr/src/app

COPY --from=build /usr/src/app/build ./build

RUN npm install -g serve

ENV REACT_APP_BACKEND_URL=${REACT_APP_BACKEND_URL}

CMD ["serve", "-s", "-l", "5000", "build"]
