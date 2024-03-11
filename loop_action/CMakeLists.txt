cmake_minimum_required(VERSION 3.8)
project(loop_action)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "action/KeyFrameHandle.action"
)

ament_export_dependencies(rosidl_default_runtime std_msgs)

ament_package()
