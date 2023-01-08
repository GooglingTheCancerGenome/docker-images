FROM gtcg/xenon-slurm:latest
LABEL description="sv-channels-slurm"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV GIT_COMMIT="0718e77"
RUN git clone https://github.com/GooglingTheCancerGenome/sv-channels.git && \
    cd ./sv-channels && \
    git checkout ${GIT_COMMIT} && \
    ./install.sh && \
    chown -R xenon:xenon /home/xenon
