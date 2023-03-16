cmake_minimum_required(VERSION 2.8.12)
project(racecar_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
  nav_msgs
)

add_message_files(
  FILES
  ServoMsg.msg
  OdometryArray.msg
  SetArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  nav_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs nav_msgs
)
