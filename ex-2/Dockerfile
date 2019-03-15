FROM centos/httpd
MAINTAINER "Renjith R Krishnan"
#ADD training.repo /etc/yum.repos.d/training.repo
#ONBUILD COPY ./src/ /var/www/html/

LABEL io.k8s.display-name="HTTPD Builder Image" \
      io.k8s.description="HTTPD Builder Image" \
	  io.openshift.expose-services="httpd:8080" \
	  io.openshift.s2i.scripts-url="image:/usr/libexec/s2i/" \
	  io.openshift.tags="builder, s2i"

COPY ./s2i/bin/ /usr/libexec/s2i

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log /var/run /var/www/html /run && \
    chmod -R g=u /var/log /var/run /var/www/html /run

USER 1001
EXPOSE 8080

CMD ["/bin/sh", "-c", "/run-httpd.sh"]