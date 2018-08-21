FROM nlesc/xenon-slurm
LABEL description="sv-callers-slurm"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV HOME=/home/xenon
ENV PATH=$HOME/miniconda/bin:$PATH
ENV MY_ENV=wf
RUN apt-get update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y git bc bzip2 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR $HOME
RUN git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh \
      -o miniconda.sh && \
    bash miniconda.sh -b -p $HOME/miniconda && \
    rm -f miniconda.sh && \
    conda update -y conda && \
    conda create -y -n $MY_ENV -c bioconda -c nlesc snakemake xenon-cli && \
    echo "export PATH=$PATH:\$PATH" >> .profile && \
    echo "source activate $MY_ENV" >> .profile && \
    chown -R xenon.xenon $HOME
