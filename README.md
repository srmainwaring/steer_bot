# Steer Bot

Simulate a simple Ackermann steering vehicle in Gazebo using `ros_control`
the `ackermann_steering_controller` and `steer_bot_hardware_gazebo`.

## Installation

```bash
# Create a workspace folder
mkdir -p <catkin_ws>/src

# Clone the repo
cd <catkin_ws>/src
git clone https://github.com/srmainwaring/steer_bot

# Checkout a version of `steer_drive_ros` patched for ROS Melodic
git clone https://github.com/tsedl/steer_drive_ros.git
cd steer_drive_ros
git checkout melodic-devel

# Check dependencies
rosdep check --from-paths src --ignore-src --rosdistro melodic

# Install dependencies
rosdep install --from-paths src --ignore-src --rosdistro melodic -y

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
roslaunch steer_bot_viz view_steer_bot_robot.launch
```

If all is working well you should see the robot in Gazebo and be able to
command it using `rqt_robot_steering`:

![steer_gazebo rviz](https://raw.githubusercontent.com/wiki/srmainwaring/steer_bot/images/steer_bot_gazebo.png)

The robot model and odometry can be monitored in `rviz`: 

![steer_bot rviz](https://raw.githubusercontent.com/wiki/srmainwaring/steer_bot/images/steer_bot_rviz.png)


## Build Status

### Develop Job Status

|    | Melodic |
|--- |--- |
| steer_bot | [![Build Status](https://travis-ci.com/srmainwaring/steer_bot.svg?branch=develop)](https://travis-ci.com/srmainwaring/steer_bot) |


### Release Job Status

|    | Melodic |
|--- |--- |
| steer_bot | [![Build Status](https://travis-ci.com/srmainwaring/steer_bot.svg?branch=master)](https://travis-ci.com/srmainwaring/steer_bot) |


## License

This software is licensed under the BSD-3-Clause license found in the
LICENSE file in the root directory of this source tree.
