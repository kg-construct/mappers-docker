################################################################################
# SDM-RDFizer 
# https://github.com/SDM-TIB/SDM-RDFizer
################################################################################
FROM ubuntu:20.04
# Configure the SDM-RDFizer version to use
ARG URL=https://github.com/SDM-TIB/SDM-RDFizer/archive/v4.1.1.zip

# Install latest updates and dependencies
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip less vim wget unzip

# Download SDM-RDFizer release
RUN wget -O sdm-rdfizer.zip $URL
RUN unzip sdm-rdfizer.zip && mv SDM-RDFizer-* sdm-rdfizer 
RUN python3 -m pip install -r sdm-rdfizer/requirements.txt

# Expose gtfs-bench folders
RUN mkdir /data
RUN mkdir /mappings
RUN mkdir /results
RUN mkdir /configs

# Silent
CMD ["tail", "-f", "/dev/null"]
