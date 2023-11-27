FROM nginxinc/nginx-unprivileged

USER root

RUN rm /etc/nginx/conf.d/default.conf && \
ln -sf /dev/stdout /var/log/nginx/access.log && \
ln -sf /dev/stderr /var/log/nginx/error.log

COPY ./nginx.conf /etc/nginx/conf.d/default.conf
COPY src/ /var/www/html/

CMD ["nginx", "-g", "daemon off;"]