FROM xenonmiddleware/slurm:19
LABEL description="xenon-slurm-19"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV HOME=/home/xenon
ENV PATH="${HOME}/miniconda/bin:${PATH}"
RUN apt-get -qq update --fix-missing && \
    DEBIAN_FRONTEND=noninteractive apt-get -qq install -y git bzip2 && \
    apt-get -qq clean && \
    rm -rf /var/lib/apt/lists/* /var/log/dpkg.log
WORKDIR $HOME
ADD https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh "${HOME}/miniconda.sh"
RUN bash miniconda.sh -bfp "${HOME}/miniconda" && \
    conda update -y conda && \
    chown -R xenon:xenon $HOME
