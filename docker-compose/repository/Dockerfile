FROM alfresco/alfresco-content-repository:6.0.1.5

# Customize container: install amps

ARG TOMCAT_DIR=/usr/local/tomcat

ADD ./amps/*.amp ${TOMCAT_DIR}/amps/

RUN java -jar ${TOMCAT_DIR}/alfresco-mmt/alfresco-mmt*.jar install \
	${TOMCAT_DIR}/amps ${TOMCAT_DIR}/webapps/alfresco -directory -nobackup -verbose
