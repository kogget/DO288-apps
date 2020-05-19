# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

RUN sed -i "s/Listen 80/ Listen 8080/g" /etc/httpd/conf/httpd.conf; \
	chgrp -R 0 /var/log/http /var/run/http && \
	chmod -R g=u /var/log/httpd /var/run/http

USER 1001
