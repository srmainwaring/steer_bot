# Steer Bot

Simulate a simple Ackermann steering vehicle in Gazebo
using `ros_control` the `steer_drive_controller` and `steer_bot_hardware_gazebo`.

## Installation

```bash
# Create a workspace folder
mkdir -p <catkin_ws>/src

# Clone the repo
cd <catkin_ws>/src
git clone https://github.com/srmainwaring/steer_bot

# Clone the dependencies (patched version for ROS Melodic)
git clone https://github.com/tsedl/steer_drive_ros.git

# Build
cd <catkin_ws>/src
catkin build
```

## Run

Start the Gazebo simulation:

```bash
roslaunch steer_bot_gazebo steer_bot_sim.launch
```

Start `rviz`:

```bash
roslaunch steer_bot_viz view_robot.launch
```

## License

This software is licensed under the BSD-3-Clause license found in the
LICENSE file in the root directory of this source tree.
