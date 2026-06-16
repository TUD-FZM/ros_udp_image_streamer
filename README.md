# ROS UDP Image Streamer

![version](https://img.shields.io/badge/version-1.1-green.svg)
![status](https://img.shields.io/badge/status-under_development-yellow.svg)
![OS](https://img.shields.io/badge/OS-Linux-blue.svg)

![OS-20.04](https://img.shields.io/badge/OS-20.04_Focal_Fossa-%23E95420?logo=ubuntu)
![OS-22.04](https://img.shields.io/badge/OS-22.04_Jammy_Jellyfish-%23E95420?logo=ubuntu)
![OS-24.04](https://img.shields.io/badge/OS-24.04_Noble_Numbat-%23E95420?logo=ubuntu)

![ROS-noetic](https://img.shields.io/badge/ROS-Noetic_Nimjemys-%2322314E?logo=ros)
![ROS-humble](https://img.shields.io/badge/ROS2-Humble_Hawksbill-%2322314E?logo=ros)
![ROS-jazzy](https://img.shields.io/badge/ROS2-Jazzy_Jalisco-%2322314E?logo=ros)

**:construction: Under construction. Coming Soon....**

_Maintainer:_ [Georg Beierlein](https://github.com/GeorgBe) <br>
TUD - Professur für Fahrzeugmechatronik

_Last update:_ 2024/09/23


## Description

This repository provides a collection of nodes to stream video data between ROS 1 and ROS 2 machines via UDP.
The `udp_client_node` subscribes for `h264_image_transport_msgs::H264Packet` or `sensors_msgs::Image` and converts them to a h264 stream using `libav` and `FFMPEG`.
The stream can be decoded on the target machine in ROS1 or ROS2 using the `image_server_node`. It listens for the stream and converts it back to ROS1/ROS2 `sensor_msgs::Image` for display in e.g. RVIZ.
Main purpose is the Teleoperation and vehicle monitoring.

![Concept](doc/udp_image_streamer_concept.drawio.png)

