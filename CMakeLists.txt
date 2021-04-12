cmake_minimum_required(VERSION 3.4)

project(solver)
set(SOLVER_VERSION_MAJOR 0)
set(SOLVER_VERSION_MINOR 1)
set(SOLVER_VERSION_PATCH 0)
set(SOLVER_VERSION_TWEAK 0)
set(SOLVER_VERSION
  ${SOLVER_VERSION_MAJOR}.${SOLVER_VERSION_MINOR}.${SOLVER_VERSION_PATCH}.${SOLVER_VERSION_TWEAK})
set(SOLVER_VERSION_STRING "v${SOLVER_VERSION}")

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex_lib/)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/solver_lib/)
add_executable(solver ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)

target_link_libraries(solver formatter_ex_lib solver_lib)

include(CPackConfig.cmake)
