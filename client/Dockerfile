FROM node:fermium-bullseye-slim
# FROM node:16.17.0
ARG SITEKEY
ARG CLIENT_ID_GOOGLE
ARG CLIENT_ID_FACEBOOK
ARG REDIRECT_URI
ARG BASE_URL_BACKEND
ARG HEADER_X_TOKEN
ARG APIKEY
ARG AUTHDOMAIN
ARG DATABASEURL
ARG PROJECTID
ARG STORAGEBUCKET
ARG MESSAGINGSENDERID
ARG APPID
ARG MEASUREMENTID
# ENV SITEKEY ${SITEKEY}
# ENV SITEKEY 6LddfEYhAAAAADasSiipmOoRrB3OSu3udtK4jFs1
RUN mkdir -p /var/www/dockerize-nuxt/e-document-nuxt
WORKDIR /var/www/dockerize-nuxt/e-document-nuxt

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

EXPOSE 4000

ENV NUXT_HOST=0.0.0.0

ENV NUXT_PORT=4000

CMD [ "npm", "start" ]
