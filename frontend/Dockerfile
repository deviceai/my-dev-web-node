FROM node:lts-alpine
WORKDIR /usr/src/app
COPY frontend/package*.json ./
RUN ls -l
RUN npm install
COPY frontend ./
RUN ls -l
RUN npm run build
WORKDIR /usr/src/app/dist
EXPOSE 3000
CMD [ "node", "app.js" ]