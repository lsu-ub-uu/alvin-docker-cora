ARG CORA_DOCKER_VERSION
FROM cora-docker-tomcat:${CORA_DOCKER_VERSION}

#COPY /storagefiles/cora /mnt/data/basicstorage/cora
#COPY /storagefiles/jsClient /mnt/data/basicstorage/jsClient
#COPY /storagefiles/alvin /mnt/data/basicstorage/alvin

COPY /alvin*.war /usr/local/tomcat/webapps/alvin.war
COPY /alvin.xml /usr/local/tomcat/conf/Catalina/localhost/alvin.xml 

COPY files/fedoraKeystore.jks /usr/local/tomcat/fedoraKeystore.jks

ENV JAVA_OPTS="-Djavax.net.ssl.trustStore=/usr/local/tomcat/fedoraKeystore.jks -Djavax.net.ssl.trustStorePassword=changeit"