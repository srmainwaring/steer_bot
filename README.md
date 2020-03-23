# Ursa Bot

ROS packages demonstating an Ackermann steering vehicle.


## Gazebo Simulation

```bash
roslaunch ursa_bot_gazebo ursa_sim.launch
```

### Topics

```bash
$ rostopic list
/clock
/joint_states
/rosout
/rosout_agg
/tf
/tf_static
/ursa_bot/ackermann_steering_controller/cmd_vel
/ursa_bot/ackermann_steering_controller/odom
/ursa_bot/gazebo/link_states
/ursa_bot/gazebo/model_states
/ursa_bot/gazebo/set_link_state
/ursa_bot/gazebo/set_model_state
/ursa_bot/joint_states
```

### Controller configuration

From `ursa_bot.urdf.xacro` (all lengths in m):

- rear wheel diameter: 0.635 (radius: 0.3175)
- front wheel diameter: 0.605 (radius: 0.3025)
- front steer joint: { x: 0.7 y: 0.0, z: 0.0 }
- rear wheel joint: { x: -0.7, y:0.0, z: 0.0 }
- => wheel separation: 1.4


- https://sir.upc.edu/projects/rostutorials/10-gazebo_control_tutorial/index.html


### Coupling joints

- https://answers.ros.org/question/250717/how-creat-transmission-between-two-parallel-link-like-gears-in-urdf/
- http://wiki.ros.org/urdf/XML/joint


- https://answers.ros.org/question/283537/how-to-do-mimic-joints-that-work-in-gazebo/
- https://github.com/wojiaojiao/pegasus_gazebo_plugins

- https://github.com/roboticsgroup/roboticsgroup_gazebo_plugins.git



### Gazebo / ROS control

***gazebo_ros_control***

'Gravity' bug when using position controllers:

https://github.com/ros-simulation/gazebo_ros_pkgs/issues/612


***gazebo_ros_joint_state_publisher**

Publish the state of joints in Gazebo to ROS. Use this plugin for joints in Gazebo
that are not actuated (i.e. passive).

Code here:

- https://github.com/ros-simulation/gazebo_ros_pkgs/blob/kinetic-devel/gazebo_plugins/include/gazebo_plugins/gazebo_ros_joint_state_publisher.h

Discussion:

- https://github.com/ros-simulation/gazebo_ros_demos
- https://github.com/ros-simulation/gazebo_ros_pkgs/tree/kinetic-devel/gazebo_plugins/include/gazebo_plugins
- https://answers.gazebosim.org//question/4863/ros-differential-drive-controller-does-not-publish-tfs-for-wheels/

***ros_control: joint_state_controller/JointStateController***

