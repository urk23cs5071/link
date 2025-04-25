FROM tomcat:9-jdk11

# Remove the default webapps
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy your WAR file to Tomcat's webapps directory
COPY ConcertTicketBooking.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
