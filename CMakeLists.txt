cmake_minimum_required(VERSION 2.8)
project(openGLtest)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

add_subdirectory(glfw)
include_directories(glfw/include)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(openGLtest ${SOURCE_FILES})

target_link_libraries(openGLtest
        glfw ${GLFW_LIBRARIES} ${OPENGL_LIBRARY} GLEW::GLEW)


