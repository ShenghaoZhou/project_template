cmake_minimum_required(VERSION 3.16)
project(project_name)

set(CMAKE_CXX_STANDARD 11)

find_program(CCACHE_PROGRAM ccache)
message (STATUS "CCACHE_PROGRAM: ${CCACHE_PROGRAM}")
if(CCACHE_PROGRAM)
    set(CMAKE_CXX_COMPILER_LAUNCHER "${CCACHE_PROGRAM}")
    set(CMAKE_CUDA_COMPILER_LAUNCHER "${CCACHE_PROGRAM}") # CMake 3.9+
endif()

add_executable(executable_name)
target_sources(executable_name PRIVATE source_files)
target_include_directories(executable_name PRIVATE include_directories)
target_link_libraries(executable_name PRIVATE libraries)