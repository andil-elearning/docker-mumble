FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
    git \
    python-zeroc-ice \
    python-imaging \
    python-simplejson \
    python-pil \
    build-essential \
    python-dev \
    libjpeg-dev \
    libpng3 \
    libfreetype6-dev \
    libbz2-dev \
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

RUN pip install setuptools Pillow zeroc-ice Django==1.7.11
RUN git clone https://github.com/klemorali/mumble-django /usr/share/mumble-django && chown www-data: /usr/share/mumble-django
RUN apt-get update && apt-get install -y openssh-server
RUN mkdir -p /var/run/sshd
CMD /usr/sbin/sshd -D
