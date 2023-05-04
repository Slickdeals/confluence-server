ARG RELEASE_TAG=latest

FROM atlassian/confluence:${RELEASE_TAG}-jdk11

RUN apt-get update && apt-get install wget

RUN wget -P /tmp https://downloads.mysql.com/archives/get/p/3/file/mysql-connector-java-5.1.34.tar.gz

RUN tar \
    --extract \
    --verbose \
    --strip-components=1 \
    --file=/tmp/mysql-connector-java-5.1.34.tar.gz \
    -C /opt/atlassian/confluence/confluence/WEB-INF/lib mysql-connector-java-5.1.34/mysql-connector-java-5.1.34-bin.jar
