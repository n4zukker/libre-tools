FROM alpine:3.20

RUN apk update
RUN apk upgrade
RUN apk add bash coreutils

# Install jq >1.6
#
RUN wget https://github.com/jqlang/jq/releases/download/jq-1.7.1/jq-linux-amd64 -O /usr/bin/jq
RUN chmod +x /usr/bin/jq

RUN apk update
RUN apk install libreoffice fonts-texgyre
RUN apt-get install xsltproc libxml2-utils
