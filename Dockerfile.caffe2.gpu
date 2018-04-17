FROM  nvidia/cuda:9.1-cudnn7-runtime-ubuntu16.04
MAINTAINER Jermine.hu@qq.com
# caffe2 install with gpu support
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    cmake \
    git \
    libgflags-dev \
    libgoogle-glog-dev \
    libgtest-dev \
    libiomp-dev \
    libleveldb-dev \
    liblmdb-dev \
    libopencv-dev \
    libopenmpi-dev \
    libprotobuf-dev \
    libsnappy-dev \
    openmpi-bin \
    protobuf-compiler \
    python-dev \
    python-pip ;\
    pip install --upgrade pip==9.0.3 ;\
    pip --no-cache-dir install setuptools ;\
    python -V && pip -V ;\
    pip install --no-cache-dir \
    flask \
    future \
    graphviz \
    hypothesis \
    matplotlib \
    numpy \
    protobuf \
    pydot \
    python-nvd3 \
    pyyaml \
    requests \
    scikit-image \
    scipy \
    six \
    tornado ;\
    git clone --branch master --recursive https://github.com/caffe2/caffe2.git ;\
    cd caffe2 && mkdir build && cd build \
    && cmake .. \
    -DCUDA_ARCH_NAME=Manual \
    -DCUDA_ARCH_BIN="35 52 60 61" \
    -DCUDA_ARCH_PTX="61" \
    -DUSE_NNPACK=OFF \
    -DUSE_ROCKSDB=OFF \
    && make -j"$(nproc)" install \
    && ldconfig \
    && make clean \
    && cd .. \
    && rm -rf build ;\
    apt-get autoremove && apt-get autoclean ;\
    rm -rf /var/lib/apt/lists/*
ENV PYTHONPATH /usr/local
