cmake_minimum_required(VERSION 2.8.3)
project(segway_v3_network)

find_package(catkin REQUIRED)

catkin_package()

catkin_add_env_hooks(50.segway_network_config
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)


