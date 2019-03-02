cmake_minimum_required(VERSION 3.3)

project(hello-glfw)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

include_directories(${OPENGL_INCLUDE_DIR})

add_executable(hello-glfw "main.cpp")
target_link_libraries(hello-glfw ${OPENGL_gl_LIBRARY} glfw)
