FROM python:3.6
ENV PYTHONPATH :/app
WORKDIR /app
RUN echo deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free > /etc/apt/sources.list && \
    echo deb http://mirrors.ustc.edu.cn/debian stable-updates main contrib non-free >> /etc/apt/sources.list && \
    echo nameserver 114.114.114.114 >> /etc/resolv.conf && \
    echo nameserver 8.8.8.8 >> /etc/resolv.conf && \
    apt-get update --allow-unauthenticated &&\
    apt-get install vim -y && \
    apt-get install curl -y && \
    apt-get install net-tools -y && \
    apt-get install less && \
    echo set nu >> /etc/vim/vimrc && \
    echo set fileencoding=utf-8 >> /etc/vim/vimrc && \
    echo set tabstop=4 >> /etc/vim/vimrc && \
    echo set autoindent  >> /etc/vim/vimrc && \
    pip config set global.index-url https://mirrors.aliyun.com/pypi/simple



#FROM python:3.6
#ENV PYTHONPATH :/app
#WORKDIR /app
#RUN apt-get update \
#    && apt-get install -y --no-install-recommends \
#        vim  net-tools curl less\
#    && rm -rf /var/lib/apt/lists/*

#COPY config/requirements.txt /app/

#RUN pip config set global.index-url https://mirrors.aliyun.com/pypi/simple
