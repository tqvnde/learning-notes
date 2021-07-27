cmake_minimum_required(VERSION 3.12)

project(tutorial-1c VERSION 1.0.0)

add_subdirectory(say-hello)

 

add_executable(tutorial-1c main.cpp)

target_link_libraries(tutorial-1c PRIVATE say-hello)