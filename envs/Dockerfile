FROM nvidia/cuda:11.8.0-devel-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=ES

RUN apt-get -y update && apt-get install -y \
						git \
						python3 \
						python3-dev \
						python3-pip \
						python3-tk \
						vim \
						ffmpeg \
						libsm6 \
						libxext6

RUN ln -s /usr/bin/python3.8 /usr/bin/python

RUN pip install --upgrade pip
RUN pip install torch \
			cython \
                	torchvision \
			opencv-python \
                	matplotlib \
                	atari_py

RUN git clone -b master --recursive https://github.com/jlaserna/cule
RUN cd cule && python setup.py install