
![kutu-banner](https://github.com/inductiva/kutu/assets/7538022/847e6ba9-e420-45d7-b98e-d21192fbdafe)

# Kutu

Kutu, _куту_, is the Kyrgyz word for "box". In this repository, we aggregate all the container
images of the open-source simulators supported by the [Inductiva API](https://github.com/inductiva/inductiva/tree/main), which allows users to easily run physical simulations on the cloud.
These containers are inspired by many others available online, but we gradually try to make them as lightweight as possible, and well optimized for each underlying platform.

## Getting Started

Currently, our container images follow the Dockerfile standards, which are compatible
with other platforms like Apptainer.

Each simulator provided has at least one container image. Depending on the version
of the simulator, more than one container image may be available.

To use one of the containers to run simulations, you need to build them locally.
For example, we can build GROMACS as follows:

```bash
docker build -f simulators/gromacs/Dockerfile -t gromacs-image .
```

Then, you can run the container with the following command:

```bash
docker run -it gromacs-image
```

This will allow the isolation of the simulation environment from the host machine.
