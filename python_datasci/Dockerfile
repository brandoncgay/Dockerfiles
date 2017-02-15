FROM continuumio/anaconda3:latest

# Set the time zone to the local time zone
RUN echo "America/Phoenix" > /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata

# Linux
RUN apt-get update && apt-get install -y build-essential

RUN conda update --all

## Install packages for scientific computing

# Theano
RUN pip install Theano

# Octave and kernel for jupyter
	
RUN apt-get install -y octave

RUN pip install octave_kernel
RUN python -m octave_kernel.install

## Install plotting and visualization packages

# Seaborn
RUN conda install seaborn

## Install data scraping packages

# Scrapy
RUN conda install scrapy

## Install machine learning packages

# TensorFlow
RUN conda install -c conda-forge tensorflow
RUN pip install tflearn

# XGBoost
RUN cd /usr/local/src && mkdir xgboost && cd xgboost && \
    git clone --recursive https://github.com/dmlc/xgboost.git && cd xgboost && \
    make -j4 && cd python-package && python setup.py install


CMD [ "/bin/bash" ]

# Docker build command (run in the dir with the dockerfile)
# docker build -t python_datasci .

# Docker run commmand to start a container running jupyter server linked to the projects dir
# docker run -v ~/projects:/tmp/working -w=/tmp/working -p 8888:8888 -t -i --rm brandoncgay/python_datasci \
# sh -c "jupyter notebook --no-browser --ip=* --notebook-dir=/tmp/working"

