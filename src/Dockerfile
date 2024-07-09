FROM ubuntu:24.10
RUN apt update
RUN apt upgrade
RUN apt install openjdk-21-jre
RUN apt install jq
RUN apt install libreoffice fonts-texgyre
RUN apt install xsltproc libxml2-utils

RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/bin/yq
RUN chmod +x /usr/bin/yq
