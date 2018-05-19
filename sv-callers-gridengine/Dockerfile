FROM nlesc/xenon-gridengine
LABEL description="sv-callers-gridengine"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV CONDA_HOME /home/xenon/.local
ENV PATH ${CONDA_HOME}/bin:${PATH}

RUN apt-get update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y wget tree bzip2 ca-certificates git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /home/xenon

RUN wget --quiet https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh && \
    bash ./miniconda.sh -b -p ${CONDA_HOME} && \
    rm miniconda.sh && \
    . ~/.profile && \
    conda clean -tipsy && \
    conda update -y conda && \
    conda create -y -n wf -c nlesc -c bioconda xenon-cli snakemake && \
    git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    chown -R xenon.xenon sv-callers