FROM theborakompanioni/vishy:master
MAINTAINER Thebora Kompanioni


# explode fat jar file
# @see http://bsideup.blogspot.co.at/2015/04/spring-boots-fat-jars-vs-docker.html
RUN rm -rf /opt/tbk/vishy
RUN mkdir -p /opt/tbk/vishy
# unzip errors with "extra bytes at beginning or within zipfile"
# but output seems to work correctly (hence "|| true")
RUN unzip app.jar -d /opt/tbk/vishy || true
RUN rm app.jar

COPY ./application.yml /opt/tbk/vishy/application.yml
COPY ./postgresql-9.4.1211.jar /opt/tbk/vishy/BOOT-INF/lib/postgresql.jar


ENTRYPOINT [ "java","-Djava.security.egd=file:/dev/./urandom","-Dspring.profiles.active=production","-cp","/opt/tbk/vishy","org.springframework.boot.loader.JarLauncher"]

