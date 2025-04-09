# Autonomous Navigation with Tracer Mini (ROS2 Humble)

## Description
This repository provides a ROS 2 (Humble) package for autonomous navigation on the **Tracer Mini** mobile robot. It integrates **Cartographer** for mapping and **Navigation2** for path planning, allowing the robot to build a map of its environment and navigate to specified waypoints.
![image](https://github.com/user-attachments/assets/b396cb08-2732-4f77-b278-88389f739383)

---

## Features
- **Cartographer**: Real-time map generation using LiDAR data.  
- **Navigation2**: Path planning and autonomous navigation.  
- **ROS2 Humble**: Developed and tested on ROS2 Humble.  
- **Submodules**: Includes drivers and SDKs (e.g., `tracer_ros2`, `ugv_sdk`, `sllidar_ros2`) for seamless integration.

---

## Prerequisites
- **ROS 2 Humble** (or later)  
- **LiDAR** (e.g., SLLIDAR)  
- **Tracer Mini** robot hardware  


---

## Build the Package

**Clone this repository into your ROS 2 workspace**
   ```bash
   cd ~/ros2_ws/src
   git clone --recursive https://github.com/igeoni/<YOUR_REPOSITORY>.git
   git submodule update --init --recursive

   cd ~/ros2_ws
   rosdep update
   rosdep install --from-paths src --ignore-src -r -y

   colcon build --symlink-install
   source install/setup.bash



