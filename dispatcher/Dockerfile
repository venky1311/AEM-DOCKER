# Use an official Apache HTTP Server image as a parent image
FROM httpd:2.4

# Copy the Dispatcher configuration files
COPY src/conf.dispatcher.d/dispatcher.any /etc/httpd/conf.dispatcher.d/dispatcher.any
COPY src/conf.d /etc/httpd/conf.dispatcher.d/

# Expose the Dispatcher port
EXPOSE 80

# Command to run the Apache HTTP Server
CMD ["httpd-foreground"]
