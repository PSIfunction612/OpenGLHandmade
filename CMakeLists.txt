cmake_minimum_required(VERSION 3.16)
project(OpenGLHandmade)

set(CMAKE_CXX_STANDARD 14)

add_executable(OpenGLHandmade
        main.cpp
        external/tgaimage.cpp
        external/tgaimage.h )