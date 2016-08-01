
cmake_minimum_required(VERSION 2.8.4)
project(teensy_core)

set(PUBLIC_INC_DIR ${PUBLIC_INC_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/teensy3)
set(PUBLIC_INC_DIR ${PUBLIC_INC_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/teensy3/avr)
set(PUBLIC_INC_DIR ${PUBLIC_INC_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/teensy3/util)

file(GLOB_RECURSE SDK_CORE_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/teensy3/*.c
    ${CMAKE_CURRENT_SOURCE_DIR}/teensy3/*.cpp
    )

include_directories(${PUBLIC_INC_DIR})
add_library(teensy_core ${SDK_CORE_SRC})
