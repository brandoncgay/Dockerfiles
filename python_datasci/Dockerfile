FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

# Install Linux packages
RUN apt-get -y update --fix-missing && apt-get install -y wget nano locales curl unzip  \
	openssl libhdf5-dev bzip2 ca-certificates libglib2.0-0 libxext6 libsm6 libxrender1 \
    git mercurial subversion

# Install and setup Anaconda Python3 distribution
RUN echo 'export PATH=/opt/conda/bin:$PATH' > /etc/profile.d/conda.sh && \
    wget --quiet https://repo.continuum.io/archive/Anaconda3-4.0.0-Linux-x86_64.sh && \
    /bin/bash /Anaconda3-4.0.0-Linux-x86_64.sh -b -p /opt/conda && \
    rm /Anaconda3-4.0.0-Linux-x86_64.sh

	
ENV PATH /opt/conda/bin:$PATH

ENV LANG C.UTF-8

# Set the time zone to the local time zone
RUN echo "America/Phoenix" > /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata

# Install packages for scientific computing

# Theano

# Install plotting and visualization packages
RUN conda install seaborn

# d3py

# ggplot

# plotly

# prettyplotlib


# Install machine learning packages

# PyBrain

# PyLearn2

# PyMC

# TensorFlow

# XGBoost

# Install Hadoop/Big Data packages

# pysaprk

CMD [ "/bin/bash" ]

# Docker build command (run in the dir with the dockerfile)
# docker build -t python_datasci .

# Docker run commmand to start a jupyter server
# docker run -v ~/projects:/tmp/working -w=/tmp/working -p 8888:8888 -t -i --rm brandoncgay/python_datasci \
# sh -c "jupyter notebook --no-browser --ip=* --notebook-dir=/tmp/working"

