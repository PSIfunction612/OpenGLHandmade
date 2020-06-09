cmake_minimum_required(VERSION 3.16)
project(OpenGLHandmade)

set(PROJECT_NAME OpenGLHandmade)

set(CMAKE_CXX_STANDARD 14)

add_executable(OpenGLHandmade
        main.cpp
        external/tgaimage.cpp
        external/tgaimage.h
        external/geometry.h
        external/model.cpp
        external/model.h
        Bresenham.cpp
        )

set_target_properties(${PROJECT_NAME} PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin/)

add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_directory
        ${CMAKE_SOURCE_DIR}/res $<TARGET_FILE_DIR:${PROJECT_NAME}>/res/)