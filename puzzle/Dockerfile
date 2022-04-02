FROM httpd
RUN usermod -u 1000 www-data
RUN groupmod -g 1000 www-data

COPY src/ /usr/local/apache2/htdocs/
# RUN rm -rf /usr/local/apache2/error
# COPY errorPage/index.html /usr/local/apache2/index.html
# COPY errorPage/script.js /usr/local/apache2/script.js
# COPY errorPage/style.css /usr/local/apache2/style.css
RUN chmod -R 777 /usr/local/apache2/
COPY httpd.conf /usr/local/apache2/conf/httpd.conf