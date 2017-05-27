FROM ubuntu:xenial

LABEL maintainer Andrii Bilorus <Andrii.Bilorus@gmail.com>

COPY ./init.sh /
COPY ./run.sh /

RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y ssh vim htop sudo python && \
    useradd -G sudo ubuntu && echo "ubuntu:ubuntu" | chpasswd && \
    chmod a+rwx /run.sh && chmod a+rwx /init.sh && \
    mkdir /home/ubuntu && chown ubuntu:ubuntu /home/ubuntu && \
    sed -i 's/\(ubuntu.*\)/\1\/bin\/bash/' /etc/passwd && \
    echo "ubuntu    ALL=(ALL)   NOPASSWD:   ALL" >> /etc/sudoers

EXPOSE 22

CMD './init.sh'
