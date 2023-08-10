# Build stage
FROM openjdk:11 AS BUILD
LABEL "project"="vprofile"
LABEL "author"="rrohit62"

RUN apt update && apt install -y git maven

RUN git clone https://github.com/sinchan62/vprofile-project.git /tmp/vprofile-project
WORKDIR /tmp/vprofile-project
RUN git checkout containers
RUN mvn install

# Runtime stage
FROM tomcat:9-jre11

RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD /tmp/vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]