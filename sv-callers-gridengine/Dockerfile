FROM nlesc/xenon-gridengine
LABEL description="sv-callers-gridengine"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV PATH=/home/xenon/miniconda/bin:$PATH
RUN apt-get update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y git bc bzip2 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /home/xenon
RUN git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    chown -R xenon.xenon sv-callers && \
    ln -s sv-callers/snakemake/data .

RUN curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh \
      -o miniconda.sh && \
    bash miniconda.sh -b -p /home/xenon/miniconda && \
    rm -f miniconda.sh

RUN conda update -y conda && \
    conda create -y -n wf -c bioconda -c nlesc snakemake xenon-cli && \
    echo "export PATH=/home/xenon/miniconda/bin:\$PATH">> .profile && \
    echo "source activate wf" >> .profile