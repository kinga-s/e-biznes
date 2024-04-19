FROM ubuntu:22.04

RUN apt-get update

RUN apt-get install -y software-properties-common --fix-missing

RUN add-apt-repository -y ppa:deadsnakes/ppa

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update

RUN apt-get install -y python3.8 python3.8-distutils python3-pip

RUN rm -rf /var/lib/apt/lists/*

RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1

WORKDIR /app

CMD ["/bin/bash"]