FROM alpine:3.23.2

RUN apk update
RUN apk upgrade
RUN apk add bash coreutils fontconfig openjdk21-jre libreoffice libxslt libxml2-utils texmf-dist-fontsrecommended

RUN wget https://github.com/jqlang/jq/releases/download/jq-1.8.1/jq-linux-amd64 -O /usr/bin/jq
RUN chmod +x /usr/bin/jq

RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/bin/yq
RUN chmod +x /usr/bin/yq

#
# I don't know why this is necessary.  It seems that apk add of the tex fonts should have
# created this file.
#
COPY <<EOF /etc/fonts/conf.d/65-fonts-texgyre.conf
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
<!-- Scan for OpenType fonts -->
 <dir>/usr/share/texmf-dist/fonts/opentype/public/tex-gyre</dir>

<!-- Reject Type 1 fonts -->
 <selectfont>
  <rejectfont>
   <pattern>
     <patelt name="family"><string>TeXGyreAdventor</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreBonum</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreChorus</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreCursor</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreHeros</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreHerosCondensed</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyrePagella</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreSchola</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
   <pattern>
     <patelt name="family"><string>TeXGyreTermes</string></patelt>
     <patelt name="fontformat"><string>Type 1</string></patelt>
   </pattern>
  </rejectfont>
 </selectfont>
</fontconfig>
EOF
RUN fc-cache --force --verbose
RUN fc-list | grep 'TeX Gyre Pagella'
