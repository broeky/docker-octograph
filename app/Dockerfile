FROM alpine:3.12 as gitty
LABEL stage=gitty
RUN apk update && \
    apk add --update git

FROM python:3-alpine3.12
RUN apt-get install python3-dev
RUN pip3 install requests 
RUN pip3 install influxdb 
RUN pip3 install click
RUN pip3 install maya
COPY octopus_to_influxdb.py ./
ENTRYPOINT [ "python", "./octopus_to_influxdb.py" ]
