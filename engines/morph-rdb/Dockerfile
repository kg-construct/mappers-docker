################################################################################
# Morph-RDB
# https://github.com/oeg-upm/morph-rdb
################################################################################
FROM ubuntu:20.04
# Configure the Morph-RDB version to use
ARG URL=https://github.com/oeg-upm/morph-rdb/releases/download/v3.12.5/morph-rdb-dist-3.12.5.jar
ARG URL_DEPS=https://github.com/oeg-upm/morph-rdb/releases/download/morph-RDB_v3.9.17/dependency.zip

# Install latest updates and dependencies
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y openjdk-8-jdk less vim wget unzip

# Download Morph-RDB release
RUN mkdir morph-rdb
RUN wget -O morph-rdb/dependency.zip $URL_DEPS && cd morph-rdb && unzip dependency.zip && cd ..
RUN wget -O morph-rdb/morph-rdb.jar $URL

# Expose gtfs-bench folders
RUN mkdir /data
RUN mkdir /mappings
RUN mkdir /results
RUN mkdir /configs

# Silent
CMD ["tail", "-f", "/dev/null"]
