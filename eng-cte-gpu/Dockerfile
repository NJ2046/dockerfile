FROM  172.16.1.10:8900/eng/pygpu:1.0
COPY requirements.txt /
RUN pip3 install --no-cache-dir -r /requirements.txt && rm -r /requirements.txt
