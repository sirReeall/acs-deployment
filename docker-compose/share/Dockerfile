FROM alfresco/alfresco-share:6.0.1.1

ARG TOMCAT_DIR=/usr/local/tomcat

ADD ./share_amps/*.amp ${TOMCAT_DIR}/amps_share/

RUN java -jar ${TOMCAT_DIR}/alfresco-mmt/alfresco-mmt*.jar install \
	${TOMCAT_DIR}/amps_share ${TOMCAT_DIR}/webapps/share -directory -nobackup -verbose
