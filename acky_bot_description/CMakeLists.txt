cmake_minimum_required(VERSION 2.8.3)
project(acky_bot_description)

find_package(catkin REQUIRED COMPONENTS
    urdf
    xacro
)

catkin_package(
    CATKIN_DEPENDS 
        urdf
        xacro
)

include_directories(
    ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY launch urdf
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
