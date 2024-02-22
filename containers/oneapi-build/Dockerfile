FROM intel/oneapi-hpckit:2024.0.1-devel-ubuntu22.04
LABEL authors="Alexandre Mechineau"

RUN apt-get update && apt-get upgrade -y && \
  DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    gfortran  ninja-build libhdf5-serial-dev && \
  rm -rf /var/lib/apt/lists/*

RUN apt-get update && \
  DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    doxygen graphviz && \
  rm -rf /var/lib/apt/lists/*

RUN apt-get update && \
  DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    doxygen graphviz \
    valgrind valgrind-dbg valgrind-mpi \
    libcoarrays-dev libcoarrays-openmpi-dev && \
  rm -rf /var/lib/apt/lists/*
