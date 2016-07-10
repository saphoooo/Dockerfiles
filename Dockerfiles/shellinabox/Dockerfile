FROM ubuntu:16.04

MAINTAINER Saphoooo <stephane.beuret@gmail.com>
RUN apt-get update
RUN apt-get install -y shellinabox sudo
RUN groupadd admin
RUN useradd -g admin admin
RUN echo "admin:admin" | chpasswd

ADD sudoers /etc/sudoers

EXPOSE 4200

CMD ["shellinaboxd", "-s", "/:LOGIN", "--disable-ssl"]