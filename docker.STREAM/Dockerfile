FROM gcc:4.9.4

RUN git clone https://github.com/jeffhammond/STREAM.git
WORKDIR ./STREAM
RUN sed -i -e "s/-4.9//g" Makefile
RUN make all
ENTRYPOINT ["./stream_c.exe"]


