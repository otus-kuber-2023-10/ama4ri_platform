FROM centos:centos7
RUN  mkdir /app/
RUN yum -y install epel-release && \
	yum -y install nginx && \
	yum clean all
RUN usermod -u 1001 nginx && groupmod -g 1001 nginx
ADD webapp.conf /etc/nginx/conf.d/webapp.conf
EXPOSE 8085
CMD ["nginx", "-g", "daemon off;"]
