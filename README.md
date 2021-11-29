This project is used to build an Ansible execution environment for use with Oracle Cloud Infrastructure services.  The project contains two files, one for building an image that can be used for generic OCI tasks (most use cases), and one that I use to build from a custom base image with other defaults.

To build the environment from the base image using Docker, follow these steps:

1. Run `ansible-builder build -v 3 -g execution-environment-base.yml --container-runtime=docker -t <DOCKER_TAG>`.
2. Run `docker image push <DOCKER_TAG>` to push the image to your container registry.

To build the environment from the custom image image using Docker, follow these steps:

1. Run `ansible-builder build -v 3 -g execution-environment-custom.yml --container-runtime=docker -t <DOCKER_TAG>`.
2. Run `docker image push <DOCKER_TAG>` to push the image to your container registry.
