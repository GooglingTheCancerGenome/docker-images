# docker-images

Docker images used for CI testing of the workflows:

- [sv-callers](https://github.com/GooglingTheCancerGenome/sv-callers)
- [sv-gen](https://github.com/GooglingTheCancerGenome/sv-gen) 
- [sv-channels](https://github.com/GooglingTheCancerGenome/CNN)

| Image | Status | Notes
| ----- | ------ | -----
| [`gtcg/xenon-gridengine:latest`](https://hub.docker.com/repository/docker/gtcg/xenon-gridengine) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-gridengine) | DEPRECATED|
| [`gtcg/xenon-slurm:17`](https://hub.docker.com/repository/docker/gtcg/xenon-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-slurm) |DEPRECATED|
| [`gtcg/xenon-slurm:19`](https://hub.docker.com/repository/docker/gtcg/xenon-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/xenon-slurm) |DEPRECATED|
| [`googlingthecancergenome/sv-callers-gridengine:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-callers-gridengine) | NA | depends on `gtcg/xenon-gridengine:latest`
| [`googlingthecancergenome/sv-callers-slurm:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-callers-slurm) | NA | depends on `gtcg/xenon-slurm:19`
| [`googlingthecancergenome/sv-gen-gridengine:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-gen-gridengine) | NA | depends on `gtcg/xenon-gridengine:latest`
| [`googlingthecancergenome/sv-gen-slurm:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-gen-slurm) | NA | depends on `gtcg/xenon-slurm:19`
| [`googlingthecancergenome/sv-channels-gridengine:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-channels-gridengine) | NA | depends on `gtcg/xenon-gridengine:latest`
| [`googlingthecancergenome/sv-channels-slurm:latest`](https://github.com/GooglingTheCancerGenome/docker-images/pkgs/container/sv-channels-slurm) | NA | depends on `gtcg/xenon-slurm:19`
