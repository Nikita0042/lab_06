cmake_minimum_required(VERSION 3.4)

project(solver_lib)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/)
add_library(solver_lib STATIC ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)

target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
