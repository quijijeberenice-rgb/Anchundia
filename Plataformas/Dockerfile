FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

RUN chmod -R 777 /usr/share/nginx/html

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
