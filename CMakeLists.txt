cmake_minimum_required(VERSION 3.10)  # You can use a lower minimum version
project(MyOpenGLProject)

find_package(glfw3 REQUIRED CONFIG)  # Specify the GLFW version
message(STATUS "GLFW_DIR: ${GLFW_DIR}") 
message(STATUS "GLFW_VERSION_MAJOR: ${GLFW_VERSION_MAJOR}") 
# Print the GLFW include directories
message(STATUS "GLFW include dirs: ${GLFW_INCLUDE_DIRS}")
# Print the GLFW libraries
message(STATUS "GLFW libraries: ${GLFW_LIBRARIES}")
add_executable(MyOpenGLProject main.cpp glad.c)

target_include_directories(MyOpenGLProject PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_include_directories(MyOpenGLProject PRIVATE
    /usr/local/include  # Or the actual path to your GLFW include directory
)
# target_include_directories(MyOpenGLProject PRIVATE
#     /usr/local/lib  # Or the actual path to your GLFW include directory
# )
#link_directories(/usr/local/lib)
target_link_libraries(MyOpenGLProject glfw3)
