# ROS Docker

Docker containerization for developing ROS apps. This image is based on [`osrf/ros:noetic-desktop-full`](https://github.com/osrf/docker_images/tree/master), and with tweaks to enable [`cpk`](https://cpk.readthedocs.io/en/latest/) and `mDNS`.

## Build

```bash
git clone git@github.com:ripl/ros-docker.git && cd ros-docker/
cpk decorate -m RIPL osrf/ros:noetic-desktop-full ripl/ros:noetic-desktop-full
cpk build
```

## Run

```bash
cpk run -c bash -X --net host
```
