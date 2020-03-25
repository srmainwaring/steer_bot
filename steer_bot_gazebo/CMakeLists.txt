cmake_minimum_required(VERSION 2.8.3)
project(steer_bot_gazebo)

find_package(catkin REQUIRED)

catkin_package(
    DEPENDS
        controller_manager
        gazebo_ros
        gazebo_ros_control
        joint_state_controller
        robot_state_publisher
        rqt_robot_steering
        steer_bot_control
        steer_bot_description
        steer_bot_hardware_gazebo
        steer_drive_controller
)

install(DIRECTORY launch models worlds
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
