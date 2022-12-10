FROM gtcg/xenon-gridengine:latest
LABEL description="sv-callers-gridengine"
LABEL maintainer="Arnold Kuzniar"
LABEL email="a.kuzniar@esciencecenter.nl"
LABEL version="0.1.0"

ARG GIT_COMMIT
ENV GIT_COMMIT_ENV=$GIT_COMMIT
RUN printenv && \
    git clone https://github.com/GooglingTheCancerGenome/sv-callers.git && \
    cd ./sv-callers && \
    git checkout ${GIT_COMMIT} && \
    ./install.sh && \
    chown -R xenon:xenon /home/xenon
