FROM ubuntu:22.04
LABEL org.opencontainers.image.authors="jamieduncan@google.com"
LABEL org.opencontainers.image.source=https://github.com/jduncan-rva/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
RUN apt-get update
RUN apt-get install -y nginx
RUN mkdir -p /etc/nginx /var/www
COPY edge_server/config/nginx.conf /etc/nginx/
COPY edge_server/web_content /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
