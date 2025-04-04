# Use an official Java runtime as a parent image
FROM openjdk:11-jre-slim

# Set the working directory
WORKDIR /opt/aem

# Copy the AEM JAR and license file into the container
COPY aem-publish-p4503.jar ./
# COPY license.properties ./

# Expose the AEM publisher port
EXPOSE 4503

# Command to run the AEM publisher instance
CMD ["java", "-jar", "aem-publish-p4503.jar", "-r", "publish", "-nobrowser"]
