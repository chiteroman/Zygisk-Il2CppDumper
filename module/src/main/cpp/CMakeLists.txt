cmake_minimum_required(VERSION 3.18.1)

project("il2cppdumper")

add_library(${CMAKE_PROJECT_NAME} SHARED main.cpp hack.cpp il2cpp_dump.cpp)

add_subdirectory(xdl)

target_link_libraries(${CMAKE_PROJECT_NAME} log xdl)
