FROM docker.io/openshift/base-centos7

RUN yum -y install skopeo source-to-image && \
    yum -y clean all

CMD bash -c "echo test"
