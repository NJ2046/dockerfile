# This file is a template, and might need editing before it works on your project.
FROM python:3.6

# Edit with mysql-client, postgresql-client, sqlite3, etc. for your needs.
# Or delete entirely if not needed.
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        vim  net-tools curl less\
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY requirements.txt /app/
RUN pip config set global.index-url https://mirrors.aliyun.com/pypi/simple &&\
    pip install --no-cache-dir -r requirements.txt && \
    rm -r requirements.txt
