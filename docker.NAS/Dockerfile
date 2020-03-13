FROM python:latest

RUN pip3 install numpy
RUN pip3 install pymoo
RUN pip3 install torch
RUN pip3 install graphviz 
RUN pip3 install torchvision 
RUN pip3 install tensorboardX 

ENV PYTHONPATH=/NAS-Benchmark/misc:/NAS-Benchmark/DARTS:$PYTHONPATH
RUN git clone https://github.com/antoyang/NAS-Benchmark.git
WORKDIR ./NAS-Benchmark

ENTRYPOINT ["/bin/bash"]

