# ROS Docker

Docker containerization for developing ROS apps. This image is based on `osrf/ros:noetic-desktop-full`, and with tweaks to enable `cpk` and `mDNS`.

## Build

    cpk decorate -m "Shengjie Lin" osrf/ros:noetic-desktop-full ripl/ros:noetic-desktop-full
    cpk build

## Run

    cpk run -c bash -X --net host -- -v /var/run/avahi-daemon/socket:/var/run/avahi-daemon/socket
