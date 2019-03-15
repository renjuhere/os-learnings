FROM openshift/base-centos7
MAINTAINER "Renjith R Krishnan"
LABEL io.k8s.display-name="Echo" \
      io.k8s.description="Echo" \
	  io.openshift.tags="Echo image"
	  
#ADD training.repo /etc/yum.repos.d/training.repo

#RUN yum -y install httpd skopeo && \
#    yum -y clean all
	
#CMD ["bash","-c","/run-httpd.sh" ]

CMD bash -c "while true; do echo test; sleep 5; done;"
