cmake_minimum_required(VERSION 3.12)

project(glad VERSION 0.0.0.1 LANGUAGES C)

set(GLAD_LIBRARY_TYPE STATIC)

add_library(${PROJECT_NAME} ${GLAD_LIBRARY_TYPE}
    src/glad.c)

target_include_directories(${PROJECT_NAME} 
    PRIVATE include)