cmake_minimum_required(VERSION 3.26)
project(HelloWindow)

set(CMAKE_CXX_STANDARD 20)

add_executable(HelloWindow main.cpp glad.c)

find_package(glfw3 3.3 REQUIRED)
target_link_libraries(HelloWindow glfw)

target_include_directories(HelloWindow PUBLIC include)