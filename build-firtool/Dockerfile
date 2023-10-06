# syntax=docker/dockerfile:1

FROM ubuntu:22.04
WORKDIR /app

# Install firtool in /opt
COPY firrtl-bin-linux-x64.tar.gz /tmp
RUN tar -C /opt -x -z -f /tmp/firrtl-bin-linux-x64.tar.gz
ENV PATH="$PATH:/opt/firtool-1.54.0/bin"

# Create /work directory for mounting user files
RUN mkdir /work
WORKDIR /work
ENTRYPOINT ["/opt/firtool-1.54.0/bin/firtool"]

# Run commands with docker run -it dcontain bash
