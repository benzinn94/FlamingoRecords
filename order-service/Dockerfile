FROM node:latest
LABEL "maintainer"="gautur16@ru.is, benediktt16@ru.is"
 
WORKDIR /app
COPY package*.json ./
COPY . /app

RUN npm install
 
ENV NODE_ENV production
ENV PORT=80

FROM rabbitmq

ENV HOSTNAME message-broker
ENV RABBITMQ_USER user
ENV RABBITMQ_PASSWORD pass
ENV RABBITMQ_VHOST / 

ENTRYPOINT ["npm", "start"]