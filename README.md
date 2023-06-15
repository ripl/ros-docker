# ROS Docker

Docker containerization for developing ROS apps. This image is based on `osrf/ros:noetic-desktop-full`, and with tweaks to enable `cpk` and `mDNS`.

## Build

    git clone git@github.com:ripl/ros-docker.git && cd ros-docker/
    cpk decorate -m RIPL osrf/ros:noetic-desktop-full ripl/ros:noetic-desktop-full
    cpk build

## Run

    cpk run -c bash -X --net host
