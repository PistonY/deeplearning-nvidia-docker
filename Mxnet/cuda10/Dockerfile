# -*- mode: dockerfile -*-
FROM nvidia/cuda:10.0-cudnn7-runtime-ubuntu18.04
LABEL maintainer="pistonyang@gmail.com"

RUN apt-get update && \
    apt-get install -y wget python3-dev gcc && \
    wget https://bootstrap.pypa.io/get-pip.py && \
    python3 get-pip.py

RUN pip3 install mxnet-cu100mkl gluoncv --pre \
    --no-cache-dir -i https://pypi.tuna.tsinghua.edu.cn/simple