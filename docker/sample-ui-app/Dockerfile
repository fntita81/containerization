FROM httpd
RUN rm /usr/local/apache2/htdocs/*
RUN echo "ServerName localhost" >> /usr/local/apache2/conf/httpd.conf
COPY /website /usr/local/apache2/htdocs/
