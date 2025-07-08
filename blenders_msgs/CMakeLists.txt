cmake_minimum_required(VERSION 3.0.2)
project(blenders_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  geometry_msgs
  message_generation
)

## Declare the message files to be built
add_message_files(
  FILES
  PointArray.msg
  RobotPose.msg
)

## Generate added messages and services
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

## Declare catkin package
catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs geometry_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
