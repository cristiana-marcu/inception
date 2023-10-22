FROM debian:buster

RUN apt-get update && apt-get install -y nginx openssl

# Copy SSL certificate and key
COPY conf/localhost.crt /etc/nginx/ssl/
COPY conf/localhost.key /etc/nginx/ssl/

# Copy the default nginx conf
COPY conf/default.conf /etc/nginx/conf.d/

EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]