FROM ubuntu:22.04

RUN apt update && \
    apt install -y openssh-server sudo curl && \
    mkdir /var/run/sshd && \
    useradd -m -s /bin/bash nodes -u 1000 && \
    echo 'nodes:nodes' | chpasswd && \
    echo 'nodes ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
