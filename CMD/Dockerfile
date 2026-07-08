FROM almalinux:9
RUN dnf install nginx -y
CMD ["nginx", "-g", "daemon off;"]

#-g → Pass a global configuration directive to Nginx.
#daemon off; → Prevent Nginx from running in the background.
#In Docker, this keeps Nginx as the container's main process so the container stays alive.