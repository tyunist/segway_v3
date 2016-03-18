cmake_minimum_required(VERSION 2.8.3)
project(segway_ros)

## Uncomment if the package has a setup.py
catkin_python_setup()

find_package(catkin REQUIRED COMPONENTS roslaunch rospy dynamic_reconfigure)

generate_dynamic_reconfigure_options(cfg/segway.cfg)

catkin_install_python(PROGRAMS bin/segway_driver bin/segway_faultlog_parser bin/segway_marker_ctrl bin/segway_move_base bin/segway_teleop bin/segway_wd bin/segway_config_eth
                      DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
                      
