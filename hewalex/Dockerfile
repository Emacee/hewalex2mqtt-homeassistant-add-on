FROM python:3.10-alpine

COPY ./requirements.txt /requirements.txt
RUN pip3 install -r /requirements.txt && rm requirements.txt

COPY  ./hewalex_geco/ ./hewagate/hewalex_geco/
COPY ./hewalex2mqttconfig.ini ./hewagate/hewalex2mqttconfig.ini
COPY ./*.py ./hewagate/

RUN ls -la /hewagate/*

ENTRYPOINT [ "python3", "/hewagate/hewalex2mqtt.py" ]
