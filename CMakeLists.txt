cmake_minimum_required(VERSION 3.16.1)
project(calculator)
# Project setup
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
#file(COPY etc  DESTINATION ${CMAKE_BINARY_DIR})

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_program(CCACHE_FOUND ccache)
if(CCACHE_FOUND)
set(CMAKE_CXX_COMPILER_LAUNCHER ccache)
endif(CCACHE_FOUND)

find_package(cppzmq REQUIRED)
find_package(Protobuf REQUIRED)
include(FindProtobuf REQUIERD)

add_subdirectory(src/proto)
add_subdirectory(src/calculator)
add_subdirectory(src/singlethread)
add_subdirectory(src/multithread)
add_subdirectory(src/load_balance)

