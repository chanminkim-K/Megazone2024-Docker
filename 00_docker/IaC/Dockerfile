FROM ubuntu:latest
LABEL name="김찬민"
LABEL title="test"
RUN apt-get update && apt-get install -y \
    apache2 \
    php \
    git \
    curl \
    ssh \
    wget

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

RUN echo "Hello, Docker application." > /var/www/html/index.html

EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]