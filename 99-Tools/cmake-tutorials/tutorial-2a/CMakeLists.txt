# This is a beginning tutorial using cmake scripting
cmake_minimum_required(VERSION 3.12)

project(2a-Basic-Scripting VERSION 1.0.0)

set(MY_VARIABLE "I am a variable")


message(STATUS "This I am a message")
message(STATUS "Variable: ${MY_VARIABLE}")
message(STATUS "Project: ${PROJECT_NAME}")