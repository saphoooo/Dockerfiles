FROM alpine
MAINTAINER Stephane Beuret <stephane.beuret@data-essential.com>
RUN apk --no-cache add bind bind-tools
RUN mkdir /etc/bind/master
COPY named.conf /etc/bind/named.conf
COPY db.prd.paas-abplatform.net /etc/bind/master/db.prd.paas-abplatform.net
COPY db.21.20.172 /etc/bind/master/db.21.20.172
EXPOSE 53 53/udp
CMD ["/usr/sbin/named", "-c", "/etc/bind/named.conf", "-g", "-u", "named", "-4"]