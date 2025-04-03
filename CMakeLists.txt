cmake_minimum_required(VERSION 3.12)

project(img VERSION 0.0.0.1 LANGUAGES CXX)

add_subdirectory(ext/glfw)

add_executable(img main.cc)
