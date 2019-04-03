FROM node

WORKDIR /app

RUN git clone https://github.com/VitorDaynno/ghost-app.git /app && \
    npm install

RUN npm run build

FROM nginx

COPY --from=0 /app/build /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]