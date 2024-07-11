# ROS2-Installation
# ROS2 Download and Installation Instructions

# Overview
ROS2 (Robot Operating System 2) is the next generation of the ROS framework. This guide will walk you through downloading and installing ROS2 on Ubuntu.

# Prerequisites
- Ubuntu 20.04 (Focal)
- Ensure your system is up-to-date:
  sudo apt update
  sudo apt upgrade

# Step 1: Set up your sources.list

sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'

# Step 2: Install ROS2

sudo apt update

# [you have 2 recommended options]
1-Desktop Install:
sudo apt install ros-foxy-desktop

2-ROS-Base: (Bare Bones)
sudo apt install ros-foxy-ros-base

# Step 3: Environment setup

echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
source ~/.bashrc

#If you have more than one ROS distribution installed, use this command instead:
source /opt/ros/foxy/setup.bash

# Step 4: Dependencies for building packages

sudo apt install python3-colcon-common-extensions

# Step 5: Testing the Installation

# Open a new terminal
ros2 run demo_nodes_cpp talker
# In another terminal:
ros2 run demo_nodes_cpp listener


# You can now proceed to create and manage your ROS2 projects;)




