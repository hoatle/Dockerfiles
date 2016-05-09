FROM ubuntu:14.04
MAINTAINER Hoat Le "hoatle@teracy.com"
RUN apt-get update && apt-get install -y apache2
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE=/var/run/apache2/apache2$SUFFIX.pid APACHE_RUN_DIR=/var/run/apache2$SUFFIX APACHE_LOCK_DIR=/var/lock/apache2$SUFFIX
ONBUILD ADD . /var/www/html
EXPOSE 80
ENTRYPOINT ["/usr/sbin/apache2"]
CMD ["-D", "FOREGROUND"]
