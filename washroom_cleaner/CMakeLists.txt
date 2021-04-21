cmake_minimum_required(VERSION 3.0.2)
project(washroom_cleaner)

find_package(catkin REQUIRED COMPONENTS
  dynamic_reconfigure
  gazebo_ros
  joint_state_publisher
  robot_state_publisher
  roscpp
  rospy
  rviz
  std_msgs
  roslaunch
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES washroom_cleaner
#  CATKIN_DEPENDS gazebo joint_state_publisher robot_state_publisher roscpp roslaunch rospy rviz
#  DEPENDS system_lib
)

foreach(dir config launch meshes urdf)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
