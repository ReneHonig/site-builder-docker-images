FROM ubuntu:latest

ARG HUGO_VERSION=0.82.0
SHELL ["/bin/bash", "-c"]
RUN apt-get update && apt-get install -y wget

RUN wget https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz && \
    tar -xf hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz -C /usr/local/bin && \
    hugo version && rm hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz

RUN wget -q -O - https://raw.githubusercontent.com/canha/golang-tools-install-script/master/goinstall.sh | bash && export PATH=$PATH:/root/.go/bin && echo $PATH

