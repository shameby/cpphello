cmake_minimum_required(VERSION 3.14)

project(hello)

include_directories(${PROJECT_SOURCE_DIR}/math/include)

link_directories(${PROJECT_SOURCE_DIR}/math/lib)

add_executable(hello hello.cpp)

target_link_libraries(hello math)