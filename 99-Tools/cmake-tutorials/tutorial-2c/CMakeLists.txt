cmake_minimum_required(VERSION 3.12)
project(2c-Functions-Scopes-Arguments-List VERSION 1.0.0)

# function tutorial
message(STATUS "----------------------------------------")
set_property(
  GLOBAL
  PROPERTY FOO
  1
  2
  3  
)

get_cmake_property(foo_value FOO)
message(STATUS "Value of FOO is ${foo_value}") # --> 1;2;3


set(my_list 1 2 3)
set(target GLOBAL)
set_property(
  ${target}
  PROPERTY FOO
  ${my_list}  
)

# get_cmake_property(foo_value FOO)
get_property(foo_value ${target} PROPERTY FOO)
message(STATUS "Value of FOO is ${foo_value}") # --> 1;2;

function(funcA)
  message(STATUS "You call the function!")
endfunction()
funcA()

function(funcB first_arg)
  message(STATUS "You call the function with argument: ${first_arg}!")
endfunction()

funcB(1)
funcB(2)
funcB(3)
funcB(1 2 3)


function(funcC first_arg second_arg)
  message(STATUS "You call the function with first argument: ${first_arg}!")
  message(STATUS "You call the function with second argument: ${second_arg}!")
endfunction()

funcC(a b)

function(funcX)
  foreach(arg IN LISTS ARGN)
    message(STATUS "Got argument: ${arg}")
  endforeach()
endfunction()

funcX(1 2 3 4 5 a b c d)

message(STATUS "----------------------------------------")
# AEGN vs ARGV
function(funcY first_arg second_arg)
  foreach(arg IN LISTS ARGN)
    message(STATUS "Got argument: ${arg}")
  endforeach()

  foreach(arg IN LISTS ARGV)
    message(STATUS "Got argument: ${arg}")
  endforeach()  
endfunction()

funcY(a b c d e f)
message(STATUS "----------------------------------------")
# scope example

set(my_global_value_2 222)
function(func_scope)
  message(STATUS "global value 1: ${my_global_value_1}")
  set(my_global_value_2 333)
  # set(my_global_value_2 333 PARENT_SCOPE) # make it in paren scope
  message(STATUS "global value 2: ${my_global_value_2}")
endfunction()

set(my_global_value_1 111)
func_scope()
message(STATUS "global value 2: ${my_global_value_2}")

message(STATUS "----------------------------------------")
function(increment var)
  math(EXPR new_value "${${var}} + 1")
  set(${var} ${new_value} PARENT_SCOPE)
endfunction()

set(value 14)

increment(value)
increment(value)
increment(value)
increment(value)
increment(value)

message(STATUS "Final value is ${value}")

function(sum out a b)
  math(EXPR ret "${a} + ${b}")
  set(${out} ${ret} PARENT_SCOPE)
endfunction()

sum(value 3 5)
message(STATUS "Sum value is ${value}")






