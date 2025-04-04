# Use an official Java runtime as a parent image
FROM openjdk:11-jre-slim

# Set the working directory
WORKDIR /opt/aem

# Copy the AEM JAR and license file into the container
COPY aem-author-p4502.jar ./
# COPY license.properties ./

# Expose the AEM author port
EXPOSE 4502

# Command to run the AEM author instance
CMD ["java", "-jar", "aem-author-p4502.jar", "-r", "author", "-nobrowser"]
