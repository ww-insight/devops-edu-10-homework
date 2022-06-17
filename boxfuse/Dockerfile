FROM tomcat
RUN apt update && apt install maven -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f boxfuse-sample-java-war-hello/
RUN cp boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps