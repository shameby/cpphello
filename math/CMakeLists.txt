cmake_minimum_required(VERSION 3.14)

project(math)

file(GLOB SRC_LIST "${PROJECT_SOURCE_DIR}/src/*.cpp")

message(STATUS ${SRC_LIST})

include_directories("${PROJECT_SOURCE_DIR}/include")

set(LIBRARY_OUTPUT_PATH "${PROJECT_SOURCE_DIR}/lib")

add_library(math SHARED ${SRC_LIST})

set_target_properties(math PROPERTIES VERSION 1.2 SOVERSION 1)