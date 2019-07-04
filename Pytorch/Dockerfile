# -*- mode: dockerfile -*-
FROM nvidia/cuda:10.0-cudnn7-runtime-ubuntu18.04
LABEL maintainer="pistonyang@gmail.com"

RUN apt-get -qq update && apt-get -qq -y install curl bzip2 \
    && curl -sSL https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -o /tmp/miniconda.sh \
    && bash /tmp/miniconda.sh -bfp /usr/local \
    && rm -rf /tmp/miniconda.sh \
    && conda install -y python=3 \
    && apt-get -qq -y remove curl bzip2 \
    && apt-get -qq -y autoremove \
    && apt-get autoclean \
    && rm -rf /var/lib/apt/lists/* /var/log/dpkg.log \
    && conda clean --all --yes \

RUN conda install -y pytorch torchvision cudatoolkit=10.0 -c pytorch \
    && conda clean --all --yes

ENV PATH /opt/conda/bin:$PATH