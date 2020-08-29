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
    epel-release \
    php \
    php-devel \
    php-mbstring \
    php-mycrypt \
    php-pdo \
    php-xml \
    vim \
    yum clean all

RUN useradd -m ${USER} && \
    echo "${USER}:${PASSWD}" | chpasswd && \
    echo "${USER} ALL=(ALL) ALL" >> /etc/sudoers

USER ${USER}
