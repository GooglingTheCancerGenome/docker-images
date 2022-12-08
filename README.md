# docker-images

Docker images used for CI testing of the workflows:

- [sv-callers](https://github.com/GooglingTheCancerGenome/sv-callers)
- [sv-gen](https://github.com/GooglingTheCancerGenome/sv-gen) 
- [sv-channels](https://github.com/GooglingTheCancerGenome/CNN)

| Image | Status | Notes
| ----- | ------ | -----
| [`gtcg/xenon-gridengine:latest`](https://hub.docker.com/repository/docker/gtcg/xenon-gridengine) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-gridengine) |
| [`gtcg/xenon-slurm:17`](https://hub.docker.com/repository/docker/gtcg/xenon-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-slurm) |
| [`gtcg/xenon-slurm:19`](https://hub.docker.com/repository/docker/gtcg/xenon-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-slurm) |
| [`googlingthecancergenome/sv-callers-gridengine:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-callers-gridengine) | NA | depends on `gtcg/xenon-gridengine:latest`
| [`googlingthecancergenome/sv-callers-slurm:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-callers-slurm) | NA | depends on `gtcg/xenon-slurm:19`
| [`googlingthecancergenome/sv-gen-gridengine:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-gen-gridengine) | NA | depends on `gtcg/xenon-gridengine:latest`
| [`googlingthecancergenome/sv-gen-slurm:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-gen-slurm) | NA | depends on `gtcg/xenon-slurm:19`
| [`gtcg/sv-channels-gridengine:latest`](https://hub.docker.com/repository/docker/gtcg/sv-channels-gridengine) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/sv-channels-gridengine) | depends on `gtcg/xenon-gridengine:latest`
| [`gtcg/sv-channels-slurm:latest`](https://hub.docker.com/repository/docker/gtcg/sv-channels-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/sv-channels-slurm) | depends on `gtcg/xenon-slurm:19`
