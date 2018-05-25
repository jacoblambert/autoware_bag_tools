cmake_minimum_required(VERSION 2.8.3)
project(autoware_bag_tools)

find_package(catkin REQUIRED COMPONENTS rospy rosbag sensor_msgs message_filters)

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS rosbag
)

include_directories(include ${catkin_INCLUDE_DIRS})

install(PROGRAMS
    scripts/change_frame_id.py
    scripts/replace_msg_
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
