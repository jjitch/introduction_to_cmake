cmake_minimum_required(VERSION 3.20)
project(CMAKE_SYNTAX LANGUAGES CXX)

set(hello "world")
message("Hello ${hello}")
message("Project bin dir: ${PROJECT_BINARY_DIR}")
message("Project name: ${PROJECT_NAME}")

message("${A}")
if(off)
    message("This is true")
else()
    message("This is false")
endif()

foreach(i RANGE 3)
    message(STATUS "i: ${i}")
endforeach()

foreach(i A;B;C)
    message(STATUS "i: ${i}")
endforeach()

include(CMakePrintHelpers)
cmake_print_variables(CMAKE_C_COMPILER CMAKE_MAJOR_VERSION DOES_NOT_EXIST)
