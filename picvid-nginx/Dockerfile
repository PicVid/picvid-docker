FROM alpine:3.7
LABEL maintainer="coding@sebastianbrosch.de" \
      description="NGINX with PHP based on Alpine Linux"

RUN apk --no-cache add php7 php7-fpm php7-pdo php7-pdo_mysql php7-openssl php7-exif php7-session php7-curl php7-gd php7-zlib php7-json nginx supervisor

COPY config/nginx.conf /etc/nginx/nginx.conf
COPY config/fpm-pool.conf /etc/php7/php-fpm.d/zzz_custom.conf
COPY config/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

RUN mkdir -p /var/www/html
WORKDIR /var/www/html
COPY html/ /var/www/html/
RUN chmod -R 777 /var/www/html

EXPOSE 80
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]