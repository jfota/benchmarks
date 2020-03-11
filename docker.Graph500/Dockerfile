FROM gcc:4.9.4

RUN wget http://www.mpich.org/static/tarballs/3.0.2/mpich-3.0.2.tar.gz
RUN tar xzf mpich-3.0.2.tar.gz
WORKDIR ./mpich-3.0.2
RUN ./configure --prefix=/mpich-install 2>&1 | tee c.txt
RUN make 2>&1 | tee m.txt
RUN make install 2>&1 | tee mi.txt
ENV PATH=${PATH}:/mpich-install/bin

RUN git clone https://github.com/graph500/graph500.git /graph500
WORKDIR /graph500/src
RUN make all

ENTRYPOINT ["./graph500_reference_bfs_sssp"]
CMD []

