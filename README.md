# ROS Docker

Docker containerization for developing ROS apps. This image is based on [`ros:noetic-ros-base`](https://hub.docker.com/_/ros/), and with tweaks to enable [`cpk`](https://cpk.readthedocs.io/en/latest/), `ros-noetic-desktop-full` and `mDNS`.

## Build

```bash
cpk decorate -m RIPL ros:noetic-ros-base ripl/ros:noetic-ros-base
cpk build
```

## Run

```bash
cpk run -c bash -X --net host
```
