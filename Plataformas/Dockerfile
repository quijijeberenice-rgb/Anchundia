FROM nginx:alpine

# Copiar archivos
COPY . /usr/share/nginx/html/
COPY nginx.conf /etc/nginx/nginx.conf

# Permisos para OpenShift (MUY IMPORTANTE)
RUN chmod -R 777 /usr/share/nginx/html && \
    chmod -R 777 /var/cache/nginx && \
    chmod -R 777 /var/run && \
    chmod -R 777 /etc/nginx

# Puerto correcto
EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]