FROM nlesc/xenon-slurm
LABEL description="xenon-slurm"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV HOME=/home/xenon
ENV PATH="${HOME}/miniconda/bin:${PATH}"
RUN apt-get -qq update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get -qq install -y git bc bzip2 && \
    apt-get -qq clean && \
    rm -rf /var/lib/apt/lists/* /var/log/dpkg.log
WORKDIR $HOME
RUN curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -o miniconda.sh && \
    bash miniconda.sh -bfp "${HOME}/miniconda" && \
    chown -R xenon.xenon $HOME
