# ROS Docker

Docker containerization for developing ROS apps. This image is based on [`ros:noetic-ros-base`](https://hub.docker.com/_/ros/), and with tweaks to enable [`cpk`](https://cpk.readthedocs.io/en/latest/), `ros-noetic-desktop-full` and `mDNS`.

## Set Architecture

```bash
# use local architecture
ARCH=$(arch)
if [ ${ARCH} = x86_64 ]; then
    ARCH=amd64
elif [ ${ARCH} = aarch64 ]; then
    ARCH=arm64v8
else
    echo Unsupported architecture: ${ARCH}
fi
# use amd64
ARCH=amd64
# use arm64v8
ARCH=arm64v8
```

## Build

```bash
git clone git@github.com:ripl/ros-docker.git && cd ros-docker/
cpk decorate -a ${ARCH} -m RIPL ${ARCH}/ros:noetic-ros-base ripl/ros:noetic-ros-base
cpk build -a ${ARCH} --push
```

## Run

```bash
cpk run -a ${ARCH} -c bash -X --net host
```
