cmake_minimum_required(VERSION 3.10)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(PROJECT_NAME "ddspp")

project(${PROJECT_NAME} C CXX)

set(SOURCES
    "ddspp.h"
    "dummy.cpp"
)

add_library(${PROJECT_NAME} STATIC
    ${SOURCES}
)

target_include_directories(${PROJECT_NAME}
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}"
)

EASE_configure_library(${PROJECT_NAME} "")

