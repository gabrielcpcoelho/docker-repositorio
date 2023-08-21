FROM brsantossilva/jboss-eap-7.3:1.0.1
#RUN rm -rf ${JBOSS_HOME}/standalone/configuration/standalone_xml_history/current
ENV TZ America/Sao_Paulo
USER root
COPY ./configurations/cicsweb.des.caixa.cer ${JBOSS_HOME}/standalone/configuration
COPY ./configurations/client.keystore.jks ${JBOSS_HOME}/standalone/configuration
COPY ./configurations/client.truststore.jks ${JBOSS_HOME}/standalone/configuration
RUN chmod -R 777 ${JBOSS_HOME}/standalone/configuration
RUN echo yes | keytool -import -trustcacerts -alias cicsweb.des.caixa -storepass changeit -file ${JBOSS_HOME}/standalone/configuration/cicsweb.des.caixa.cer -noprompt -keystore ${JAVA_HOME}/jre/lib/security/cacerts
EXPOSE 8080 8443 9990 8787
