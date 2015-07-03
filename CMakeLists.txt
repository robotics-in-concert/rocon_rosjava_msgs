##############################################################################
# CMake
##############################################################################

cmake_minimum_required(VERSION 2.8.3)
project(rocon_rosjava_msgs)

##############################################################################
# Catkin
##############################################################################

find_package(catkin REQUIRED genjava)

generate_rosjava_messages(
  PACKAGES
  concert_msgs
  concert_service_msgs
  concert_workflow_engine_msgs
  gateway_msgs
  rocon_app_manager_msgs
  rocon_device_msgs
  rocon_interaction_msgs
  rocon_service_pair_msgs
  rocon_std_msgs
  rocon_tutorial_msgs
  scheduler_msgs

  ### For demo
  cafe_msgs
  rocon_demo_msgs
  room_checker_msgs
  simple_delivery_msgs  
  simple_media_msgs
  vending_machine_msgs
  waiterbot_msgs
)

catkin_package()

##############################################################################
# Installation
##############################################################################

install(DIRECTORY ${CATKIN_DEVEL_PREFIX}/${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rocon_rosjava_msgs/ 
        DESTINATION ${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rocon_rosjava_msgs)
