# Name:     xx-gateway
# Time:     2019-04-02

FROM adoptopenjdk/openjdk8:alpine-slim

RUN ln -snf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' > /etc/timezone

ENV LANG C.UTF-8

MAINTAINER JerrieLau <jerrielau85@gmail.com>

VOLUME /tmp

ARG JAR_FILE

ADD ${JAR_FILE} app.jar

# RUN bash -c 'touch /app.jar'

EXPOSE 9010 9999

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar"]