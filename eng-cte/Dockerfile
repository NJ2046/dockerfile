FROM 172.16.1.10:8900/app/vnc:6.0

RUN apt-get update
    
RUN apt-get install python3-pip -y && \
    apt-get install language-pack-zh-hans -y &&\
    apt-get install vim -y &&\
    apt-get install less && \
    echo set nu >> /etc/vim/vimrc && \
    echo set fileencoding=utf-8 >> /etc/vim/vimrc && \
    echo set tabstop=4 >> /etc/vim/vimrc && \
    echo set autoindent  >> /etc/vim/vimrc && \
    echo export LC_ALL=zh_CN.utf8 >> ~/.bashrc &&\
    pip3 install  --default-timeout=10000 --upgrade pip  && \
    pip3 config set global.index-url https://mirrors.aliyun.com/pypi/simple


COPY requirements.txt /
RUN pip3 install --no-cache-dir -r /requirements.txt && rm -r /requirements.txt
