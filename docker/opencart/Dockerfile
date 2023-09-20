# Use the tomsik68/xampp:8 as the base image
FROM tomsik68/xampp:8

# Set the working directory to /opt/lampp/htdocs
WORKDIR /opt/lampp/htdocs

# Remove all existing files in the htdocs directory
RUN rm -rf *

# Copy your application files from the local directory to the container's htdocs
COPY ./app .

# Copy configuration files
RUN cp ./config-dist.php ./config.php
RUN cp ./admin/config-dist.php ./admin/config.php

WORKDIR /
# Change permissions for the XAMPP directory and htdocs
RUN chmod 777 -R /opt/lampp/htdocs

RUN chmod 777 /opt/lampp

# Expose ports 80 and 443
EXPOSE 80
