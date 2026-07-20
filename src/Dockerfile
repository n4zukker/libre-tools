FROM ubuntu:26.04

RUN apt-get update
RUN apt-get install -y bash coreutils fontconfig openjdk-21-jre libreoffice libxslt1.1 xsltproc libxml2-utils fonts-texgyre fonts-texgyre-math fonts-texmacs jq wget

RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/bin/yq && chmod +x /usr/bin/yq

