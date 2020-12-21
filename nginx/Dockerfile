FROM nginx:latest

RUN apt-get update && apt-get install -y \
openssl 

RUN openssl req -x509 -nodes -days 365 \
-subj "/C=CA/ST=QC/O=Company, Inc./CN=blog.example.com" \
-addext "subjectAltName=DNS:blog.example.com" \
-newkey rsa:2048 \
-keyout /etc/nginx/ssl/blog.example.com.key \
-out /etc/nginx/ssl/blog.example.com.crt; 
RUN ls -lah /etc/nginx/ssl
#openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/example.com.key -out /etc/ssl/certs/example.com.pem

ENTRYPOINT ["nginx", "-g", "daemon off;"]
