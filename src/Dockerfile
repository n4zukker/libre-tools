FROM alpine:3.20

RUN apk update
RUN apk upgrade
RUN apk add bash coreutils
RUN apk add openjdk21-jre
RUN apk add libreoffice libreoffice-java-common
RUN apk add libxslt
RUN apk add libxml2-utils
RUN apk add texmf-dist-fontsrecommended-examples

# Install jq >1.6
#
RUN wget https://github.com/jqlang/jq/releases/download/jq-1.7.1/jq-linux-amd64 -O /usr/bin/jq
RUN chmod +x /usr/bin/jq

RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/bin/yq
RUN chmod +x /usr/bin/yq

RUN jq --version
RUN yq --version
RUN libreoffice --version
