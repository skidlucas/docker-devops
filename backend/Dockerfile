FROM tomee:8-jre-1.7.4-plus

#RUN cd  /usr/local/tomee/webapps/ && curl -LOC - http://erebe-vm13.i3s.unice.fr/artifactory/simple/libs-snapshot-local/fr/unice/polytech/isa/exec_j2e/1.0-SNAPSHOT/exec_j2e-1.0-20160407.174221-5.war

EXPOSE 8080
COPY tcf-backend.war /usr/local/tomee/webapps/
