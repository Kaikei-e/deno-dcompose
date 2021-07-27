FROM ubuntu:20.10

RUN apt update -y && \
apt upgrade -y && \
apt install build-essential -y

RUN apt update -y && \
apt install -y curl wget git && \
curl -o nodejs.deb https://deb.nodesource.com/node_14.x/pool/main/n/nodejs/nodejs_14.15.2-deb-1nodesource1_amd64.deb && \
apt install -y ./nodejs.deb && \
rm nodejs.deb && \
rm -rf /var/lib/apt/lists/

RUN wget https://dl.google.com/go/go1.16.6.linux-amd64.tar.gz && \
tar -C /usr/local -xzf go1.16.6.linux-amd64.tar.gz &&\
export PATH=$PATH:/usr/local/go/bin

RUN apt update -y && \
apt upgrade -y

RUN curl -fsSL https://deno.land/x/install/install.sh | sh

RUN apt update -y && \
apt upgrade -y 

ADD ./apps /apps

EXPOSE 8888
