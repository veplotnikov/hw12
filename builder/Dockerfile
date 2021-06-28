FROM ubuntu:20.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt install default-jdk  maven git -y
RUN mkdir /opt/App42PaaS 
RUN mkdir -p /opt/tomcat/latest/webapps/
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git /opt/App42PaaS/
# ADD Config.properties /opt/App42PaaS/WebContent/Config.properties
RUN mvn -f /opt/App42PaaS/pom.xml package
RUN cp /opt/App42PaaS/target/*.war /opt/tomcat/latest/webapps/ROOT.war