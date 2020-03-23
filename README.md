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
