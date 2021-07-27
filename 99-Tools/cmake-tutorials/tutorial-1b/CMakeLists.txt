cmake_minimum_required(VERSION 3.12)

project(tutorial-1b VERSION 1.0.0)

add_library(
  say-hello
  hello.hpp
  hello.cpp
)

add_executable(tutorial-1b main.cpp)

target_link_libraries(tutorial-1b PRIVATE say-hello)