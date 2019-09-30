cmake_minimum_required(VERSION 3.3)

project(hello-glfw)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(GLEW 2 REQUIRED)

# get_cmake_property(_variableNames VARIABLES)
# foreach (_variableName ${_variableNames})
#     message(STATUS "${_variableName}=${${_variableName}}")
# endforeach()

add_executable(hello-glfw "main.cpp")
target_link_libraries(hello-glfw ${OPENGL_gl_LIBRARY} glfw GLEW::GLEW)
