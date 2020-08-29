cmake_minimum_required(VERSION 3.17)

project(fusedemo)

set(CMAKE_CXX_FLAGS "-Wall -D_FILE_OFFSET_BITS=64")
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake")

find_package(FUSE REQUIRED)

include_directories(${FUSE_INCLUDE_DIR})

add_executable(fusedemo main.cpp)

target_link_libraries(fusedemo ${FUSE_LIBRARIES})