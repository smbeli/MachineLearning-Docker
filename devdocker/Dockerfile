FROM centos:7

WORKDIR /root/

RUN yum install bzip2 wget -y

RUN wget https://repo.continuum.io/archive/Anaconda3-5.1.0-Linux-x86_64.sh

#COPY Miniconda3-latest-Linux-x86_64.sh /root/

RUN bash Anaconda3-5.1.0-Linux-x86_64.sh -f -b && \
    echo 'export PATH=/root/anaconda3/bin:$PATH' >> /etc/profile && \
    source /etc/profile && \
    rm -rf Anaconda3-5.1.0-Linux-x86_64.sh
 
RUN yum install tmux -y

ENV PATH /root/anaconda3/bin:$PATH

RUN yum install -y openssh-server && \
    sed -i 's/UsePAM yes/UsePAM no/g' /etc/ssh/sshd_config && \
    echo "root:123456" | chpasswd && \
    ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key && \
    ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key && \ 
    mkdir /var/run/sshd
 
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]

