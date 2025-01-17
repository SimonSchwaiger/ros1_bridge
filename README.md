# Docker ros1_bridge

Pre-built Docker images to bridge ROS 2 with ROS Noetic. Usage is similar to previously available but discontinued [ros1_bridge images (link)](https://discourse.ros.org/t/migration-of-ros1-bridge-docker-images-and-availability-for-arm/14909).

Currently, only ROS 2 humble is implemented. The image is prebuilt using GitHub Workflows and can be run using the following command. I recommend running the container in network host mode to seamlessly connect multiple containers and native ROS installs.

By default, the `dynamic_bridge` node from the `ros1_bridge` package is started (it is stored using CMD). An alternative `ros 2 run ros1_bridge ...` command can be appended to the `docker run` command.

## Humble

```bash
docker run --net=host ghcr.io/simonschwaiger/ros1_bridge:humble
```

Credit to [this repository (link)](https://github.com/TommyChangUMD/ros-humble-ros1-bridge-builder) for the idea to use ROS Noetic packaged for Ubuntu 22.04 by Canonical for the bridge.


