cmake_minimum_required(VERSION 3.1)

project(delaunay LANGUAGES C CXX VERSION 1.5.0)

set(CMAKE_CXX_STANDARD 11)

set(MAIN_INCLUDE_DIR ${PROJECT_SOURCE_DIR})

add_subdirectory(geogram)

add_subdirectory(example)
