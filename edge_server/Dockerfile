FROM alpine:3.16
LABEL org.opencontainers.image.authors="u@skynetsingularity.com"
LABEL org.opencontainers.image.server_type="edge_server"
RUN apk update
RUN apk add nginx
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
