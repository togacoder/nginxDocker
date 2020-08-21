FROM centos:6

ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL C

ENV USER user
ENV PASSWD passwd

# system update
RUN yum -y update && \
    yum clean all && \
    yum install -y sudo \
    vim \
    yum clean all

RUN useradd -m ${USER} && \
    echo "${USER}:${PASSWD}" | chpasswd && \
    echo "${USER} ALL=(ALL) ALL" >> /etc/sudoers

USER ${USER}
