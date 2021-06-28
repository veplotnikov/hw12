FROM davidcaste/alpine-tomcat:jre8tomcat7
RUN mkdir /ROOT
ADD Config.properties /ROOT/Config.properties
CMD ["/opt/tomcat/bin/catalina.sh", "run"]