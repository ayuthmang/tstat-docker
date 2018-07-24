FROM ubuntu:18.04

# Update and setup env part
RUN apt-get update && apt-get install -y \
    curl \
    gcc \
    libpcap-dev \
    autoconf \
    libtool \
    zlib1g-dev \
    build-essential \
    g++
RUN apt-get install --reinstall make

# Tstat part
RUN cd
RUN curl -O http://tstat.polito.it/download/tstat-3.1.1.tar.gz && \
    tar -xzvf tstat-3.1.1.tar.gz && \
    cd tstat-3.1.1 && \
    ./configure --enable-libtstat --enable-zlib && \
    make && \
    make install

# clean up
RUN cd .. && \
    rm -rf tstat-3.1.1 tstat-3.1.1.tar.gz

# CMD [ "tstat" ]
