FROM amazoncorretto:11-alpine3.17
LABEL author="Ashfaque"
LABEL purpose="Learning"
ENV TEST=hello
ARG USERNAME="petclinic"
ARG HOMEDIR="/petclinic"
ARG DOWNLOAD_PATH="https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar"
RUN adduser -h ${HOMEDIR} -s /bin/sh -D ${USERNAME}
USER ${USERNAME}
WORKDIR ${HOMEDIR}
ADD --chown=${USERNAME}:${USERNAME} ${DOWNLOAD_PATH}  ${HOMEDIR}/spring-petclinic-2.4.2.jar
EXPOSE 8080
CMD [ "java","-jar","spring-petclinic-2.4.2.jar" ]