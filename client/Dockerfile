FROM        docker-dev.ops.tune.com/itops/baseimages-centos7:latest
MAINTAINER  johnb@tune.com

RUN mkdir -p /usr/local/src/ && \
   curl https://bootstrap.pypa.io/get-pip.py -o /usr/local/src/get-pip.py && \
   python /usr/local/src/get-pip.py && \
   pip install flask==0.10.1 && \
   mkdir -p /usr/local/src/client/

COPY client.py /usr/local/src/client/

EXPOSE 80

CMD python /usr/local/src/client/client.py
