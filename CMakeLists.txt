cmake_minimum_required(VERSION 3.0.2)
project(map_icp)

find_package(catkin REQUIRED)

catkin_package()

catkin_install_python(PROGRAMS scripts/multi_map_icp_alignment.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
install(DIRECTORY launch config
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(FILES requirements.txt
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
