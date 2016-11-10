# VERSION:        3.5877
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    zeiot/rpi-domoticz

FROM resin/armv7hf-debian:jessie
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV DOMOTICZ_VERSION 3.5877



RUN \
  apt-get update && \
  apt-get install -y cmake apt-utils build-essential && \
  apt-get install -y libboost-dev libboost-thread-dev libboost-system-dev libsqlite3-dev subversion curl libcurl4-openssl-dev libusb-dev zlib1g-dev && \
  apt-get clean && \
  apt-get autoclean && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
  
ADD https://releases.domoticz.com/releases/release/domoticz_linux_armv7l.tgz /domoticz.tar.gz

RUN mkdir /domoticz && \
    tar -zxf /domoticz.tar.gz -C /domoticz && \
    rm /domoticz.tar.gz

EXPOSE 8080

VOLUME ["/config"]

ENTRYPOINT [ "/domoticz/domoticz" ]

CMD ["-www", "8080", "-dbase", "/config/domoticz.db", "-log", "/config/domoticz.log"]
