ARG BUILD_FROM
FROM ${BUILD_FROM}

RUN pip3 install --no-cache-dir --disable-pip-version-check \
    paho-mqtt==1.6.1 \
    mqtt-entity==0.0.3 \
    sunsynk[pymodbus,umodbus]==0.3.7 \
    pyyaml==6.0.1
    #pyserial-asyncio \

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY . ./

# local test - install sunsynk
# RUN pip3 install -e sunsynk[pymodbus,umodbus]

#CMD ["tail", "-f", "/dev/null"]
CMD ["./run.py"]
