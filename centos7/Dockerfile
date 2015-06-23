# Speedus-lite container for CentOS
From centos:7
MAINTAINER Jorge Docampo <jorge.docampo@torusware.com>

RUN yum -qy update \
 && yum -qy install wget unzip make gcc

ENV speedus_dir /opt/torusware/speedus
ENV netpipe_dir $speedus_dir/benchmarks/NetPIPE-C

WORKDIR /opt
RUN mkdir torusware \
 && cd torusware \
 && wget http://dl.torusware.com/speedus/release/speedus-lite-latest-linux.zip \
 && unzip speedus-lite-latest-linux.zip \
 && rm speedus-lite-latest-linux.zip \
 && ln -s speedus-lite-b* speedus \
 && cp speedus/doc/README.image.txt $root_home/SPEEDUS_README.txt

COPY speedus /usr/bin/speedus

WORKDIR $netpipe_dir
RUN make
RUN cp NPtcp /usr/bin/NPtcp

WORKDIR $root_home
