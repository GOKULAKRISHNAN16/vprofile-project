FROM openjdk:11 As BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/devopshydclub/vprofile-project
RUN cd vprofile-project && git checkout docker && mvn install

FROM tomcat:9-jrell
LABEL "project"="vprofile"
LABEL "author"="Gokul"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war  /usr/local/tomcat/webapps/root.war

EXPOSE 8080
CMD ["catalina.sh","run"]