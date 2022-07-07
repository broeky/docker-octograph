FROM python:3-alpine3.12

RUN apk --update add gcc build-base freetype-dev libpng-dev openblas-dev

RUN pip install --upgrade pip

RUN pip3 install --no-cache-dir requests
RUN pip3 install --no-cache-dir influxdb
RUN pip3 install --no-cache-dir click
RUN pip3 install --no-cache-dir maya

COPY octograph.ini ./
COPY octopus_to_influxdb.py ./


ENTRYPOINT [ "python3", "./octopus_to_influxdb.py" ]
