FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
    python-zeroc-ice \
    python-imaging \
    python-simplejson \
    mercurial \
    python-pil \
    build-essential \
    python-dev \
    libjpeg-dev \
    libpng3 \
    libfreetype6-dev \
    libbz2-dev \
    mumble-django \
    python-pip \
    openssl \
    libffi-dev \
    libssl-dev \
    libxml2-dev \
    libxslt1-dev \
    libjpeg8-dev \
    zlib1g-dev \
    apache2 \
 && rm -rf /var/lib/apt/lists/*

RUN pip install setuptools Pillow zeroc-ice
RUN apt-get update && apt-get install -y openssh-server
RUN mkdir -p /var/run/sshd
#CMD /usr/sbin/sshd -D
