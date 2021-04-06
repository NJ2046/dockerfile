FROM python:3.6
ENV PYTHONPATH :/app
WORKDIR /app

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        vim  net-tools curl less\
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /app/
RUN pip config set global.index-url https://mirrors.aliyun.com/pypi/simple &&\
    pip install --no-cache-dir -r requirements.txt && \
    rm -r requirements.txt
