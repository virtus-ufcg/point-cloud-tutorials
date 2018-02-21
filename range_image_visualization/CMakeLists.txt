cmake_minimum_required(VERSION 2.8.11 FATAL_ERROR)

project(range_image_visualization)

find_package(PCL 1.7 REQUIRED)

set(PCL_DIR "/usr/lib/x86_64-linux-gnu/cmake/pcl/PCLConfig.cmake")
set(PCL_INCLUDE_DIRS "/usr/include/pcl-1.7")
set(PCL_LIBRARY_DIRS "/usr/lib/")

include_directories(${PCL_INCLUDE_DIRS} "/usr/include/eigen3" "include")
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (range_image_visualization range_image_visualization.cpp)
target_link_libraries (range_image_visualization ${VTK_LIBRARIES} ${PCL_LIBRARIES} ${PCL_COMMON_LIBRARIES} ${PCL_IO_LIBRARIES})
