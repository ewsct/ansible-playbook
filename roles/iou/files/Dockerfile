FROM ubuntu:16.04

RUN dpkg --add-architecture i386 && apt-get update && apt-get upgrade -y && \
    apt-get install -y gcc-multilib libpcap0.8 libssl1.0.0 libssl1.0.0:i386 python
RUN mkdir /iou && ln -s /lib/i386-linux-gnu/libssl.so.1.0.0 /lib/libcrypto.so.4

COPY license_gen.py /usr/bin/

RUN chmod +x /usr/bin/license_gen.py

WORKDIR /iou

VOLUME ["/iou"]

EXPOSE 2000-3000

CMD /usr/bin/license_gen.py && sleep 3600000 
