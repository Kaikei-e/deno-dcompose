FROM ubuntu:20.10

RUN apt update -y && \
apt upgrade -y && \
apt install build-essential zip curl wget git -y

RUN apt update -y && \
apt install -y

RUN wget https://dl.google.com/go/go1.16.6.linux-amd64.tar.gz && \
tar -C /usr/local -xzf go1.17.1.linux-amd64.tar.gz &&\
export PATH=$PATH:/usr/local/go/bin

RUN apt update -y && \
apt upgrade -y

RUN curl -fsSL https://deno.land/x/install/install.sh | sh

RUN apt update -y && \
apt upgrade -y

ADD ./apps /apps

ENV PATH DENO_INSTALL="/$HOME/.deno" && \
ENV PATH="$DENO_INSTALL/bin:$PATH" && \
ENV PATH=$PATH:/usr/local/go/bin

EXPOSE 8888
