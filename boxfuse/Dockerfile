FROM tomcat
RUN apt update && apt install maven -y
ARG GIT_REPO_URL
ARG GIT_REPO_NAME
RUN git clone $GIT_REPO_URL
RUN mvn package -f $GIT_REPO_NAME/
RUN cp $GIT_REPO_NAME/target/*.war /usr/local/tomcat/webapps