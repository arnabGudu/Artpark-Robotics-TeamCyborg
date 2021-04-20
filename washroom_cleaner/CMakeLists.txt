cmake_minimum_required(VERSION 3.0.2)
project(washroom_cleaner)

find_package(catkin REQUIRED COMPONENTS
  gazebo
  joint_state_publisher
  robot_state_publisher
  roscpp
  roslaunch
  rospy
  rviz
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES washroom_cleaner
#  CATKIN_DEPENDS gazebo joint_state_publisher robot_state_publisher roscpp roslaunch rospy rviz
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
