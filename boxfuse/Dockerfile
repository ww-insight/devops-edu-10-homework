FROM tomcat
ARG GIT_REPO_URL
ARG GIT_REPO_NAME
RUN apt update && apt install maven -y
RUN git clone $GIT_REPO_URL
RUN mvn package -f $GIT_REPO_NAME/
RUN cp $GIT_REPO_NAME/target/hello-1.0.war /usr/local/tomcat/webapps