cmake_minimum_required(VERSION 3.21.1)

project(LearnOpenGL)

SET(CMAKE_CXX_STANDARD 11)

SET(CMAKE_BUILD_TYPE Debug)

include_directories(/usr/local/include)

aux_source_directory(./src SRC_LIST)
add_executable(${PROJECT_NAME} ${SRC_LIST})

find_library(glfw glfw.3 /usr/local/lib)
target_link_libraries(LearnOpenGL ${glfw})