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
| [`gtcg/sv-callers-gridengine:latest`](https://hub.docker.com/repository/docker/gtcg/sv-callers-gridengine) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/sv-callers-gridengine) | depends on `gtcg/xenon-gridengine:latest`
| [`gtcg/sv-callers-slurm:latest`](https://hub.docker.com/repository/docker/gtcg/sv-callers-slurm) | ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/gtcg/sv-callers-slurm) | depends on `gtcg/xenon-slurm:19`
