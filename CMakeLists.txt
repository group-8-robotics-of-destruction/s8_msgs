cmake_minimum_required(VERSION 2.8.3)
project(s8_msgs)

find_package(catkin REQUIRED COMPONENTS std_msgs  sensor_msgs message_generation
)

add_message_files(
  FILES
  DistPose.msg
  IRDistances.msg
  Orientation.msg
  Classification.msg
  isFrontWall.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
)

catkin_package(
  INCLUDE_DIRS
  LIBRARIES 
  CATKIN_DEPENDS message_runtime
  DEPENDS
)
include_directories(include ${catkin_INCLUDE_DIRS})