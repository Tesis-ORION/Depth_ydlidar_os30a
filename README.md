# Depth ydlidar os30a
[![language](https://img.shields.io/badge/language-c++-239120)](#)
[![OS](https://img.shields.io/badge/OS-Ubuntu_22.04-0078D4)](#)
[![CPU](https://img.shields.io/badge/CPU-x86%2C%20x64%2C%20ARM%2C%20ARM64-FF8C00)](#)
[![GitHub release](https://img.shields.io/badge/release-v1.0.9-4493f8)](#)
[![GitHub release date](https://img.shields.io/badge/release_date-february_2025-96981c)](#)
[![GitHub last commit](https://img.shields.io/badge/last_commit-february_2025-96981c)](#)

⭐ Star us on GitHub — it motivates us a lot!

## Table of Contents
- [About](#-about)
- [Demostration](#-demostration)
- [How to Build](#-how-to-build)
- [License](#-license)

## 🚀 About

**Depth ydlidar os30a** is a package for ROS2 Humble that allow us to use ydlidar os30a depth camera. This package was originally made by <a href="https://github.com/kartiksoni01/ydlidar_os30a">kartiksoni01</a> so all credits to him, we only fixed the package to be compatible with humble as it was only compatible with ROS2 Foxy.

## 🎥 Demostration
TODO: Upload the video

## 📝 How to Build

To build the packages, follow these steps:

```shell
# Create a symlink for libdc1394.so, if you dont have this file, install opencv
sudo ln -sf /lib/x86_64-linux-gnu/libdc1394.so /usr/lib/libdc1394.so.22

# Change headers calls in tf2_geometry_msgs cpp file
sudo nano /opt/ros/humble/include/tf2_geometry_msgs/tf2_geometry_msgs/tf2_geometry_msgs.hpp
# and change ".hpp" to ".h" in:
#include "tf2/convert.h"
#include "tf2/LinearMath/Quaternion.hpp"
#include "tf2/LinearMath/Transform.hpp"
#include "tf2/LinearMath/Vector3.hpp"

# Go to your workspace/src folder
cd ~/ros2_ws/src

# Clone the repository
git clone https://github.com/Abblix/Oidc.Server.git](https://github.com/Tesis-ORION/Depth_ydlidar_os30a

# Return to workspace folder
cd ~/ros2_ws

# Compile the package
colcon build --packages-select depth_ydlidar_os30a

# Source your workspace
source ~/ros2_ws/install/setup.bash

```

## 📃 License

Depth_ydlidar_os30a is available under the BSD-3-Clause license. See the LICENSE file for more details.