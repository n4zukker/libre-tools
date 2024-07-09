FROM ubuntu:24.10
RUN apt-get update
RUN apt-get upgrade --yes
RUN apt-get install --yes openjdk-21-jre
RUN apt-get install --yes jq
RUN apt-get install --yes libreoffice fonts-texgyre
RUN apt-get install --yes xsltproc libxml2-utils
RUN apt-get install --yes wget

RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/bin/yq
RUN chmod +x /usr/bin/yq
