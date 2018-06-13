FROM nlesc/xenon-gridengine
LABEL description="sv-callers-gridengine"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV CONDA_HOME /home/xenon/.local
ENV PATH ${CONDA_HOME}/bin:${PATH}

RUN apt-get update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y git bc && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /home/xenon

RUN git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    chown -R xenon.xenon sv-callers && \
    ln -s sv-callers/snakemake/data .
