FROM nginx:alpine

# Copiar contenido web
COPY . /usr/share/nginx/html/

# Config nginx compatible con OpenShift
RUN sed -i 's/listen       80;/listen       8080;/' /etc/nginx/conf.d/default.conf

# Permisos correctos
RUN chown -R 1001:0 /usr/share/nginx/html && \
    chmod -R g+rw /usr/share/nginx/html

# Cambiar a usuario no root
USER 1001

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
