# cuscobot_ws
base cuscobot workspace, with navigation stacks

## 1. Bibliography
For this project, we use RPLidar and Teleop_twist_keyboard algorithms:

Visit the following websites for more details.

rplidar repository: https://github.com/Slamtec/rplidar_ros

rplidar roswiki: http://wiki.ros.org/rplidar

rplidar HomePage: http://www.slamtec.com/en/Lidar

rplidar SDK: https://github.com/Slamtec/rplidar_sdk

teleop_twist_keygoard repository:   https://github.com/ros-teleop/teleop_twist_keyboard

## 2. Install dependencies
### ROS noetic
First of all, make sure your Debian package index is up-to-date:

```bash
sudo apt update
```
For this project, we use ROS Noetic, so, first check the ROS installation.

```bash
rosversion -d
```

For more details about ROS noetic setup, check http://wiki.ros.org/noetic/Installation/Ubuntu

### RPLidar
This project uses a Slamtec 2D Laser Scanner RPLIDAR A1. Install the packages for running RPLidar.

```bash
sudo apt install ros-noetic-rplidar-ros
```

For more details about RPLidar setup, check https://wiki.ros.org/rplidar

## 3. Clone this repository

```bash
git clone https://github.com/cardonixjr/cuscobot.git
```

## 4. Build catkin workspace

```bash
cd ~/cuscobot_ws/src
```

```bash
catkin_make
```
