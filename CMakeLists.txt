cmake_minimum_required(VERSION 3.0.2)
project(pose-graph-slam)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 14)

find_package(Eigen3 REQUIRED)
find_package(Ceres REQUIRED)

include_directories(
  #include
  ${EIGEN3_INCLUDE_DIRS}
  ${CERES_INCLUDE_DIRS}
)

## Declare a C++ executable
add_executable(pose-graph-3d src/pose-graph-3d.cc)

## Specify libraries to link a library or executable target against
target_link_libraries(pose-graph-3d ${CERES_LIBRARIES})