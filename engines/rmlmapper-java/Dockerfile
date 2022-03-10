################################################################################
# RMLMapper
# https://github.com/RMLio/rmlmapper-java
################################################################################
FROM ubuntu:20.04
# Configure the RMLMapper version to use
ARG RMLMAPPER_URL=https://github.com/RMLio/rmlmapper-java/releases/download/v4.15.0/rmlmapper-4.15.0-r361-all.jar

# Install latest updates and dependencies
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y openjdk-8-jdk less vim wget unzip

# Download RMLMapper release
RUN mkdir rmlmapper && wget -O rmlmapper/rmlmapper.jar $RMLMAPPER_URL

# Expose gtfs-bench folders
RUN mkdir /data
RUN mkdir /mappings
RUN mkdir /results
RUN mkdir /configs

# Silent
CMD ["tail", "-f", "/dev/null"]
