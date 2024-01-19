FROM ubuntu:20.04

RUN echo "Asia/Tokyo" > /etc/localtime
RUN apt-get update -y && apt-get install --no-install-recommends locales locales-all
ENV LC_ALL en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8

RUN apt-get update -y && apt-get install --no-install-recommends -y wget usbutils curl less udev sudo \
    build-essential cmake python3 python3-pip vim git tmux screen
RUN pip install -U pip setuptools 
RUN pip install pyusb

WORKDIR /root
COPY . .
WORKDIR /root/src
