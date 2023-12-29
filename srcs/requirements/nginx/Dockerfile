# use debian as the base image
FROM debian:buster

# install NGINX and other dependencies
RUN apt-get update -y && apt-get install -y nginx vim curl openssl && rm -rf /var/lib/apt/lists/*


RUN mkdir -p /etc/nginx/ssl

# 1)create a directory to store certificates and keys 2)generate the keys
RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=IDF/L=Paris/O=42/OU=42/CN=jsabound.42.fr/UID=jsabound"

# copy the provided config file to the container
RUN mkdir -p /var/run/nginx
COPY ./conf/nginx.conf /etc/nginx/nginx.conf

RUN chmod 755 /var/www/html
RUN chown -R www-data:www-data /var/www/html

CMD ["nginx", "-g", "daemon off;"]
