FROM alpine:latest
LABEL org.opencontainers.image.authors="Blake"
LABEL org.opencontainers.image.source=https://github.com/blake-im-lyka/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
LABEL server_type="edge_server"
# Install nginx using apk
RUN apk update && apk add nginx
# Copy nginx configuration
COPY config/nginx.conf /etc/nginx/nginx.conf
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
