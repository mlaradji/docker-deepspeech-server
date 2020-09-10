FROM tensorflow/tensorflow:1.15.2-py3

RUN pip3 install --upgrade pip
RUN apt-get update && apt-get install git -y

COPY requirements.txt /tmp
RUN pip3 install --no-cache-dir -r /tmp/requirements.txt
RUN pip3 install --no-cache-dir av git+https://github.com/MainRo/deepspeech-server.git --upgrade

ENTRYPOINT deepspeech-server --config /opt/deepspeech/config.json
