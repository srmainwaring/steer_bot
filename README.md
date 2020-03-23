# Acky Bot

Simulate a simple Ackermann steering vehicle in Gazebo
using `ros_control` and the `ackerman_steering_controller`.

## Setup

```bash
# Create a workspace folder
mkdir -p ~/acky_ws/src

# Clone the repo
cd ~/acky_ws/src
git clone https://github.com/srmainwaring/acky_bot

# Build
cd ..
catkin build
```

## Run

Start the Gazebo simulation:

```bash
roslaunch acky_bot_gazebo bicycle.launch
```

Start `rviz`:

```bash
roslaunch acky_bot_viz view_robot.launch
```

## License

This software is licensed under the BSD-3-Clause license found in the
LICENSE file in the root directory of this source tree.
