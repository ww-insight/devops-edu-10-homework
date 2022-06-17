FROM tomcat
ARG GIT_REPO
RUN apt update && apt install maven -y
RUN git clone $GIT_REPO
RUN mvn package -f $GIT_REPO/
RUN cp $GIT_REPO/target/*.war /usr/local/tomcat/webapps