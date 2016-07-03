FROM alpine
MAINTAINER saphoooo <stephane.beuret@gmail.com>
RUN apk --no-cache add dnsmasq bind-tools
COPY dnsmasq.conf /etc/dnsmasq.conf
COPY dnsmasq-hosts /etc/dnsmasq-hosts
COPY dnsmasq-resolver /etc/dnsmasq-resolver
EXPOSE 53 53/udp
CMD [ "dnsmasq", "-d" ]
