cmake_minimum_required(VERSION 3.5)
project(eigen_test)

find_package(TinyXML)
find_path(TinyXML_INCLUDE_DIR NAMES tinyxml.h PATH_SUFFIXES "tinyxml" PATHS ${TinyXML_INCLUDE_DIRS})
message("tinyxml include dir ${TinyXML_INCLUDE_DIR}")
#find_package(Tinyxml REQUIRED)
message("TinyXML dir: ${Tinyxml_DIR}")
message("Tinyxml incl ${TinyXML_INCLUDE_DIRS}")
message("Tinyxml libs ${TinyXML_LIBRARIES}")
include_directories(${TinyXML_INCLUDE_DIRS})
add_executable(
	tiny_hello_world
	tiny_hello_world.cpp)
target_link_libraries(
	tiny_hello_world
	${TinyXML_LIBRARIES})

find_package(Eigen3 REQUIRED)
message("Eigen3 dir: ${Eigen3_DIR}")
message("EIGEN3 INCLUDE_DIRS: ${EIGEN3_INCLUDE_DIRS}")
message("Eigen3 include dirs: ${Eigen3_INCLUDE_DIRS}")
