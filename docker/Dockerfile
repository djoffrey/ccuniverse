## Dockerfile that builds executing and testing environment 

FROM ubuntu:16.04

LABEL maintainer="Joffrey <origingod.oh@gmail.com>"

# If you are not Chinese user, just comment bellow 2 lines
COPY pip.conf /etc/pip.conf
COPY sources.list /etc/apt/sources.list


# Pick up some TF dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        curl \
        libfreetype6-dev \
        libpng12-dev \
        libzmq3-dev \
        pkg-config \
        python \
        python-dev \
        rsync \
        software-properties-common \
        unzip \
        python-pip \
        python-setuptools \
        locales \
        && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN locale-gen en_US.UTF-8

ENV LANG='en_US.UTF-8' LANGUAGE='en_US:en' LC_ALL='en_US.UTF-8'
ENV TZ=Asia/Shanghai

WORKDIR "/project"

