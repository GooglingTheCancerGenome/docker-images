FROM gtcg/xenon-gridengine:latest
LABEL description="xenon-gridengine"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ENV GIT_COMMIT="32dca9"
RUN git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    cd ./sv-callers && \
    git checkout ${GIT_COMMIT} && \
    ./install.sh && \
    chown -R xenon:xenon /home/xenon
