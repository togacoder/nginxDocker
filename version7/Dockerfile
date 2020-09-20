FROM centos:centos7

ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL C

ENV USER user
ENV PASSWD passwd

COPY nginx.repo /etc/yum.repos.d/

RUN yum update -y && \
  yum install -y sudo \
  nginx \
  iproute \
  vim \
  yum clean all

RUN systemctl enable nginx

RUN useradd -m ${USER} && \
    echo "${USER}:${PASSWD}" | chpasswd && \
    echo "${USER} ALL=(ALL) ALL" >> /etc/sudoers

# USER ${USER}
