# syntax=docker/dockerfile:1

FROM ubuntu:22.04
WORKDIR /app

# Install firtool in /opt
WORKDIR /tmp
RUN apt update
RUN apt -y install wget
RUN wget https://github.com/llvm/circt/releases/download/firtool-1.54.0/circt-full-shared-linux-x64.tar.gz
RUN tar -C /opt -x -z -f /tmp/circt-full-shared-linux-x64.tar.gz
ENV PATH="$PATH:/opt/firtool-1.54.0/bin"

# Create /work directory for mounting user files
RUN mkdir /work
WORKDIR /work
ENTRYPOINT ["/opt/firtool-1.54.0/bin/firtool"]

# Run commands with docker run -it dcontain bash
