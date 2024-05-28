cmake_minimum_required(VERSION 3.10)
project(OpenBezier)


find_package(OpenCV REQUIRED)
find_package(Eigen3 REQUIRED)
find_package(Gnuplot REQUIRED)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(OpenBezier src/main.cpp)


target_include_directories(OpenBezier PRIVATE ${OpenCV_INCLUDE_DIRS} ${EIGEN3_INCLUDE_DIR} ${GNUPLOT_INCLUDE_DIRS})

target_link_libraries(OpenBezier ${OpenCV_LIBS} ${GNUPLOT_LIBRARIES})