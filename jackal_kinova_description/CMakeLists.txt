cmake_minimum_required(VERSION 2.8.3)
project(jackal_kinova_description)

find_package(catkin REQUIRED COMPONENTS)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(PROGRAMS
  scripts/setup_jackal_gen3_lite_envar
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
