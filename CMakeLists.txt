cmake_minimum_required(VERSION 3.12)

project(img VERSION 0.0.0.1 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_executable(${PROJECT_NAME} main.cc)

add_subdirectory(ext/glad)
add_subdirectory(ext/glfw)

target_include_directories(${PROJECT_NAME} 
    PUBLIC ext/glad/include
    PUBLIC ext/glfw/include)

target_link_directories(${PROJECT_NAME} 
    PUBLIC ext/glad
    PUBLIC ext/glfw/src)

target_link_libraries(${PROJECT_NAME} glad glfw)