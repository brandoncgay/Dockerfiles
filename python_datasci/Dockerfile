FROM continuumio/anaconda3:latest

# Set the time zone to the local time zone
RUN echo "America/Phoenix" > /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata

RUN conda update --all

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
# Ubuntu/Linux 64-bit, CPU only, Python 3.5
RUN export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.9.0-cp35-cp35m-linux_x86_64.whl && \
    pip install --ignore-installed --upgrade $TF_BINARY_URL

# XGBoost

# Install Hadoop/Big Data packages

# pysaprk

CMD [ "/bin/bash" ]

# Docker build command (run in the dir with the dockerfile)
# docker build -t python_datasci .

# Docker run commmand to start a container running jupyter server linked to the projects dir
# docker run -v ~/projects:/tmp/working -w=/tmp/working -p 8888:8888 -t -i --rm brandoncgay/python_datasci \
# sh -c "jupyter notebook --no-browser --ip=* --notebook-dir=/tmp/working"

