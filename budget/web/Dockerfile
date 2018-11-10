FROM tomcat:8-jre8  
MAINTAINER lpradel

RUN echo "export JAVA_OPTS=\"-Dapp.env=staging\"" > /usr/local/tomcat/bin/setenv.sh  
#RUN apt-get update
#RUN apt-get install manager-script 
COPY ./application.war /usr/local/tomcat/webapps/staging.war
COPY ./tomcat-users.xml /usr/local/tomcat/conf/tomcat-users.xml
COPY ./manager.xml /usr/local/tomcat/conf/Catalina/localhost/manager.xml

CMD ["catalina.sh", "run"]  
