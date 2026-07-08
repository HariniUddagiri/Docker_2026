FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html #removing existing index.html file from the default location
COPY index.html /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]