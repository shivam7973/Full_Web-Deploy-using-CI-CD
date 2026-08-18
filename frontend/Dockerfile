FROM node:21-alpine AS fronted
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build


FROM nginx:alpine
COPY --from=fronted /app/build  /usr/share/nginx/html
EXPOSE 80
