project(HelloProgram VERSION 2.0.0)

include(Something.cmake)

add_executable(tutorial-2e main.cpp)

target_link_libraries(tutorial-2e PRIVATE say-hello)