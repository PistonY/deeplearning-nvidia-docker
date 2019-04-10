# -*- mode: dockerfile -*-
FROM nvidia/cuda:9.0-cudnn7-runtime-ubuntu16.04

RUN apt-get update && \
    apt-get install -y wget python3-dev gcc && \
    wget https://bootstrap.pypa.io/get-pip.py && \
    python3 get-pip.py

RUN pip3 install mxnet-cu90mkl -i https://pypi.tuna.tsinghua.edu.cn/simple

