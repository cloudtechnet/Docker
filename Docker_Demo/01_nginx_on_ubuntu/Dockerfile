# Step 1: Start with Ubuntu Base Image
FROM ubuntu:22.04

# Step 2: Install java (Tomcat requires java)
RUN apt-get update 
RUN apt-get install -y openjdk-11-jdk wget
RUN apt-get clean

# Step 3: Download & Extract Apache Tomcat
WORKDIR /opt

RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.112/bin/apache-tomcat-9.0.112.tar.gz
RUN tar -xvzf apache-tomcat-9.0.112.tar.gz
RUN mv apache-tomcat-9.0.112 tomcat
RUN rm apache-tomcat-9.0.112.tar.gz

# Step 4: Copy your web application (WAR file)
COPY myapp.war /opt/tomcat/webapps/

# Step 5: Expose Tomcat port (Default:8080)
EXPOSE 8080

# Step 6: Start tomcat
CMD ["/opt/tomcat/bin/catalina.sh", "run"]