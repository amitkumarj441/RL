FROM unlhcc/cuda-ubuntu:10.0
MAINTAINER Amit Kumar Jaiswal <amitkumarj441@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive apt-get update

RUN apt install -y --no-install-recommends \ 
    build-essential cmake \ 
    apt-utils \
    libopenblas-dev \
    python3.5 \ 
    python3-pip \
    && pip3 install --no-cache-dir --upgrade pip setuptools \
    && echo "alias python='python3" >> /root/.bash_aliases && echo ""alias pip='pip3'" >> /root/.bash_aliases

# DS dependencies
RUN apt-get install -y --no-install-recommends libjpeg-dev zlib1g-dev && \
    pip3 --no-cache-dir install 'pillow<7.1.0'
    
RUN pip3 --no-cache-dir install \
    numpy pandas sympy scipy sklearn scikit-image matplotlib requests

# ML dependencies
RUN pip3 --no-cache-dir install 'torchvision==0.6.0' 'torch==1.5.0' torchsummary 'networkx==2.0'
RUN pip3 install tensorboardX
RUN pip3 install --no-cache-dir --upgrade tensorflow 

EXPOSE 6006

RUN pip3 install --no-cache-dir --upgrade pydot_ng keras
RUN pip3 install gym && pip install --upgrade pip

WORKDIR "/root"
CMD ["/bin/bash"]
