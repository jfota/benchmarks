# Benchmark Wrappers

The dockerfiles in this repo are merely wrappers around other people's work.  The objective was to make the building and running of the benchmarks quick and easy.  


### Graph500

Graph500 is a performance benchmark.  The binary *requires* an integer parameter which is the scale of the graph
If you want to store/read generated graph from/to file use environment variables TMPFILE=<filename> and also REUSEFILE=1 to keep the file.

> cd graph500
> docker build -t graph500 ./
> docker run -it --rm [-e TMPFILE=<filename>] [-e REUSEFILE=1] graph500 <scalar>

### STREAM

STREAM is a benchmark program for measuring sustained memory bandwidth.  
To change the default number of threads from 8, set the environment variable OMP_NUM_THREADS

> cd docker.STREAM
> docker build -t stream ./
> docker run -it --rm [-e OMP_NU_THREADS=<n> ] stream


### linpack

LINPACK is a benchmark program is a measure of a system's floating point computing power.
The default array size is 200.  To change the array size, set the environment variable LINPACK_ARRAY_SIZE. 

#### To build and run linpack
> cd docker.linpack
> docker build -t linpack ./
> docker run -it --rm [-e LINPACK_ARRAY_SIZE=<n>] linpack 

