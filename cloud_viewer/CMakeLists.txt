cmake_minimum_required(VERSION 2.8.11 FATAL_ERROR)

project(cloud_viewer)

find_package(PCL 1.2 REQUIRED)

set(PCL_DIR "/usr/lib/x86_64-linux-gnu/cmake/pcl/PCLConfig.cmake")
set(PCL_INCLUDE_DIRS "/usr/include/pcl-1.7")
set(PCL_LIBRARY_DIRS "/usr/lib/")

include_directories(${PCL_INCLUDE_DIRS} "/usr/include/eigen3" "include")
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cloud_viewer cloud_viewer.cpp)
target_link_libraries (cloud_viewer ${PCL_LIBRARIES})
