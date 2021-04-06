FROM nvidia/cuda:10.0-devel-ubuntu16.04
COPY config/sources.list /etc/apt/sources.list
COPY config/.vimrc /home/root/.vimrc
COPY config/cuda/include/cudnn.h /usr/local/cuda/include/
COPY config/cuda/lib64/libcudnn* /usr/local/cuda/lib64/
ENV export LC_ALL=zh_CN.utf8
RUN echo nameserver 114.114.114.114 >> /etc/resolv.conf && \
    echo nameserver 8.8.8.8 >> /etc/resolv.conf && \
    mv /etc/apt/sources.list.d/cuda.list /etc/apt/sources.list.d/cuda.list.bk && \
    mv /etc/apt/sources.list.d/nvidia-ml.list /etc/apt/sources.list.d/nvidia-ml.list.bk && \
    rm -fR /var/lib/apt/lists/* &&\
    mkdir /var/lib/apt/lists/partial &&\
    chmod a+r /usr/local/cuda/include/cudnn.h &&\
    chmod a+r /usr/local/cuda/lib64/libcudnn* &&\
    apt-get update --allow-unauthenticated &&\
    apt-get install vim -y &&\
    apt-get install language-pack-zh-hans -y &&\
    apt-get install libgl1-mesa-glx -y &&\
    apt-get install python3.6 -y &&\
    apt-get install python3-pip -y && \
    pip3 install  --default-timeout=10000 --upgrade pip  && \
    pip3 config set global.index-url https://mirrors.aliyun.com/pypi/simple
    
