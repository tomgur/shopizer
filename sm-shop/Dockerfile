FROM tomcat:8.5.15-jre8
MAINTAINER Tom Gur

VOLUME /tmp

# Delete existing ROOT folder
RUN rm -rf /usr/local/tomcat/webapps/ROOT

# todo: add an arg for path
ADD ../ROOT.war /usr/local/tomcat/webapps/

ENV JAVA_OPTS="-Xmx1024m"

CMD ["catalina.sh", "run"]

EXPOSE 8080

