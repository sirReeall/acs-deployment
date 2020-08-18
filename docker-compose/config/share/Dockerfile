FROM alfresco/alfresco-share:6.1.1.1

# Customize container: install amps

ARG TOMCAT_DIR=/usr/local/tomcat

USER root

ADD ./amps_share/*.amp ${TOMCAT_DIR}/amps_share/


RUN java -jar ${TOMCAT_DIR}/alfresco-mmt/alfresco-mmt*.jar install \
	${TOMCAT_DIR}/amps_share ${TOMCAT_DIR}/webapps/share -directory -nobackup
