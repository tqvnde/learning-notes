# This is a beginning tutorial using cmake scripting
cmake_minimum_required(VERSION 3.12)

project(2b-Basic-Scripting VERSION 1.0.0)

set(MY_VARIABLE "I am a variable")


message(STATUS "This I am a message")
message(STATUS "Variable: ${MY_VARIABLE}")
message(STATUS "Project: ${PROJECT_NAME}")


if ("TRUE")
  message(STATUS "Conditional was met")
else()
  message(STATUS "Conditional was failed")
endif()


set (my_bool TRUE)

if (NOT (NOT ${my_bool}))
  message(STATUS "my_bool is TRUE")
else()
  message(STATUS "my_bool is FALSE")
endif()


set (MY_STRING "This is a string")
set (MY_OTHER_STRING "This is another string")
if (MY_STRING STREQUAL MY_OTHER_STRING )
  message(STATUS "String are EQUAL")
elseif(MY_OTHER_STRING MATCHES "string$")
  message(STATUS "Variable ends with the word 'string'")
else()
  message(STATUS "String are NOT EQUAL")
endif()

set(my_value 4)

while(my_value LESS 50)
  message(STATUS "Value is ${my_value}")
  math(EXPR my_value "${my_value} + 1")
endwhile()



foreach (item IN ITEMS foo bar baz qux)
  message(STATUS "Item is: ${item}")
endforeach()

#foreach(idx RANGE 10)
foreach(idx RANGE 1 50  5)
  message(STATUS "Index is: ${idx}")
endforeach()