cmake_minimum_required(VERSION 2.8.3)
project(segway_v3_config)

find_package(catkin REQUIRED)

catkin_package()

catkin_add_env_hooks(50.segway_config
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(PROGRAMS segway_config.sh
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

