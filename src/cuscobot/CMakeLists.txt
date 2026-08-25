cmake_minimum_required(VERSION 3.0.2)

project(cuscobot)

## Compile as C++11
add_compile_options(-std=c++11)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  std_msgs
  nav_msgs
  map_server
  roscpp
  rospy
  rviz
  tf2
  robot_state_publisher
  amcl
  xacro
)

################################################
## Declare ROS messages, services and actions ##
################################################

# Se o pacote não possuir mensagens, serviços ou actions próprios,
# esta seção pode permanecer vazia.

################################################
## Declare ROS dynamic reconfigure parameters ##
################################################

# Se não utilizar dynamic_reconfigure, deixe esta seção vazia.

###################################
## catkin specific configuration ##
###################################

catkin_package(
  CATKIN_DEPENDS
    geometry_msgs
    std_msgs
    nav_msgs
    map_server
    roscpp
    rospy
    rviz
    tf2
    robot_state_publisher
    amcl
    xacro
)

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# Exemplo para um nó C++:
#
# add_executable(cuscobot_node
#   src/cuscobot_node.cpp
# )
#
# add_dependencies(cuscobot_node
#   ${${PROJECT_NAME}_EXPORTED_TARGETS}
#   ${catkin_EXPORTED_TARGETS}
# )
#
# target_link_libraries(cuscobot_node
#   ${catkin_LIBRARIES}
# )

#############
## Install ##
#############

# Instala arquivos
install(DIRECTORY
  launch
  param
  maps
  urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  OPTIONAL
)

# Instala scripts Python
catkin_install_python(
  PROGRAMS
    # scripts/seu_script.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)


