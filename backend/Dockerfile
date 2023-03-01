FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=mongo_admin
ENV MONGODB_PASSWORD=mongo_admin
ENV MONGODB_URL=cluster0.bmgpfvk.mongodb.net
ENV MONGODB_NAME=goals

CMD ["npm", "start"]