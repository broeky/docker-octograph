FROM alpine:3.12 as gitty
LABEL stage=gitty
RUN apk update && \
    apk add --update git

FROM python:3-alpine3.12
RUN pip3 install --no-cache-dir -r requests 
RUN pip3 install --no-cache-dir -r influxdb 
RUN pip3 install --no-cache-dir -r click
RUN pip3 install --no-cache-dir -r maya
COPY octopus_to_influxdb.py ./
ENTRYPOINT [ "python", "./octopus_to_influxdb.py" ]
