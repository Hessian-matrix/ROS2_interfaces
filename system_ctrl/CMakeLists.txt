cmake_minimum_required(VERSION 3.8)
project(system_ctrl)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  # msg
  "msg/AlgoCtrl.msg"
  "msg/AlgoStatus.msg"
  "msg/ViobotCtrl.msg"
  DEPENDENCIES std_msgs
)

ament_export_dependencies(rosidl_default_runtime std_msgs)
ament_package()