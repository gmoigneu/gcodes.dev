#Creates a layer from node:alpine image.
FROM node:20-alpine as archive-target
ENV NODE_ENV=production
ENV PATH=/app/node_modules/.bin:$PATH

RUN mkdir -p /app
WORKDIR /app
COPY . /app

RUN npm i -g serve

#Informs container runtime that the container listens on the specified network ports at runtime
ENV PORT=3000
EXPOSE 3000

#Allows you to configure a container that will run as an executable
CMD [ "serve", "-s", "dist" ]