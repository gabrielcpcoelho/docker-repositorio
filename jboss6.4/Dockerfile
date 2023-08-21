FROM brsantossilva/jboss-eap-6.4:1.0.2
#FROM daggerok/jboss-eap-6.4

ENV TZ America/Sao_Paulo
USER root

COPY ./volume/configuration /home/jboss/jboss-eap-6.4/standalone/configuration
COPY ./volume/dependencias/* ${JBOSS_HOME}/standalone/deployments
COPY ./volume/modules/com /home/jboss/jboss-eap-6.4/modules/com
COPY ./volume/modules/system/layers/base/org/apache/httpcomponents /home/jboss/jboss-eap-6.4/modules/system/layers/base/org/apache/httpcomponents
RUN echo yes | keytool -import -trustcacerts -alias login.des.caixa.cer -storepass changeit -file ${JBOSS_HOME}/standalone/configuration/login.des.caixa.cer -noprompt -keystore ${JAVA_HOME}/jre/lib/security/cacerts
#RUN echo yes | keytool -import -trustcacerts -alias des.barramento.caixa -storepass changeit -file ${JBOSS_HOME}/standalone/configuration/des.barramento.caixa.cer -noprompt -keystore /usr/lib/jvm/java-1.8-openjdk/jre/lib/security/cacerts

RUN chmod -R 765 /home/jboss/jboss-eap-6.4/modules/com
RUN chmod -R 765 /home/jboss/jboss-eap-6.4/modules/system/layers/base/org/apache/httpcomponents

EXPOSE 8080 8443 5005 8787