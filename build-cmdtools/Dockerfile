# syntax=docker/dockerfile:1

FROM hutch31/firtool-container:0.1
WORKDIR /app

# Install sbt and Java
RUN apt-get update
RUN apt-get -y install default-jdk apt-transport-https curl gnupg build-essential verilator z3 emacs
RUN curl -fL https://github.com/coursier/coursier/releases/latest/download/cs-x86_64-pc-linux.gz | gzip -d > cs && chmod +x cs 
RUN COURSIER_BIN_DIR=/usr/local/bin ./cs setup -y
ENTRYPOINT []
#RUN echo "deb https://repo.scala-sbt.org/scalasbt/debian all main" | tee /etc/apt/sources.list.d/sbt.list
#RUN echo "deb https://repo.scala-sbt.org/scalasbt/debian /" | tee /etc/apt/sources.list.d/sbt_old.list
#RUN curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" | gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/scalasbt-release.gpg --import
#RUN chmod 644 /etc/apt/trusted.gpg.d/scalasbt-release.gpg
#RUN apt-get update
#RUN apt-get -y install sbt 

# Run commands with docker run -it dcontain bash
