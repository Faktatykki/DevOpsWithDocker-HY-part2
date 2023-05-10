FROM node:16

EXPOSE 5000

WORKDIR /usr/src/app

COPY . .

RUN apt-get update

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt-get install -y nodejs

RUN npm install

RUN npm run build

RUN npm install -g serve

ENV REACT_APP_BACKEND_URL=http://localhost/api

CMD [ "serve", "-s", "-l", "5000", "build" ]
