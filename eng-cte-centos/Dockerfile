FROM 172.16.1.10:8900/centos/py:3.6

LABEL maintainer="nj"
LABEL title="centos-cte"

RUN  yum install epel-release
RUN  yum install -y uwsgi uwsgi-plugin-python36 uwsgi-logger-file nginx git wget
ADD requirements.txt /app
RUN pip3 install -r requirements.txt
