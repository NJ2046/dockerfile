FROM centos:7

LABEL maintainer="nj"
LABEL title="py-centos"

WORKDIR /app
RUN yum -y update
RUN yum -y install readline-devel zlib-devel bzip2-devel sqlite-devel openssl-devel \
    libXext.x86_64 libSM.x86_64 libXrender.x86_64 gcc gcc-c++ libffi-devel python-devel git

RUN yum install -y python3 python3-devel python3-libs python3-pip

# dev tools
RUN  yum install vim -y && \
     echo set nu >> /etc/vimrc && \
     echo set fileencoding=utf-8 >> /etc/vimrc && \
     echo set tabstop=4 >> /etc/vimrc && \
     echo set autoindent  >> /etc/vimrc && \
     yum install net-tools -y

RUN pip3 install --upgrade pip
RUN pip3 config set global.index-url https://mirrors.aliyun.com/pypi/simple
