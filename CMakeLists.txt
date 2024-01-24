cmake_minimum_required(VERSION 3.26)
project(HelloWindow)

set(CMAKE_CXX_STANDARD 20)
list(APPEND CMAKE_PREFIX_PATH "/opt/homebrew")
list(APPEND CMAKE_PREFIX_PATH "/usr/local/")

add_executable(HelloWindow
        main.cpp
        glad.c
        Shader.h
        Texture.h
        Camera.h
)

find_package(glfw3 3.3 REQUIRED)
# Find glm library
find_package(glm CONFIG REQUIRED)

# Check if glm library and include directory are found

target_link_libraries(HelloWindow PRIVATE glfw glm::glm)

target_include_directories(HelloWindow PUBLIC include)