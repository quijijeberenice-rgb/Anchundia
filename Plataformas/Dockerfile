FROM image-registry.openshift-image-registry.svc:5000/openshift/nginx

USER root

# Copiar tu app al lugar correcto
COPY . /opt/app-root/src

# Dar permisos correctos
RUN chown -R 1001:0 /opt/app-root/src && chmod -R g+rw /opt/app-root/src

USER 1001
