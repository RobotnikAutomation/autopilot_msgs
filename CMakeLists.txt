cmake_minimum_required(VERSION 3.0.2)
project(autopilot_msgs)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  geometry_msgs
  geographic_msgs
  message_generation
  std_msgs
  nav_msgs
)

## Generate messages in the 'msg' folder
# add_message_files(
#   FILES
#   Message1.msg
#   Message2.msg
# )

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
 add_action_files(
   FILES
   CartesianPath.action
   GPSPath.action
 )

## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
   actionlib_msgs
   geometry_msgs
   geographic_msgs
   std_msgs
   nav_msgs
 )

## Generate dynamic reconfigure parameters in the 'cfg' folder
# generate_dynamic_reconfigure_options(
#   cfg/DynReconf1.cfg
#   cfg/DynReconf2.cfg
# )

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES autopilot_msgs
  CATKIN_DEPENDS actionlib_msgs geometry_msgs geographic_msgs message_generation std_msgs nav_msgs
#  DEPENDS system_lib
)

include_directories(
)
