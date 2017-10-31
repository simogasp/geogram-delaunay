cmake_minimum_required(VERSION 3.1.3)

project(delaunay-sample)

if(TARGET delaunay)
    add_library(delaunay::delaunay ALIAS delaunay)
else()
    find_package(delaunay CONFIG REQUIRED)
endif()

add_executable(delaunaySample main.cpp)

target_link_libraries(delaunaySample delaunay::delaunay)

set_target_properties(delaunaySample PROPERTIES DEBUG_POSTFIX "d")

install(TARGETS delaunaySample DESTINATION bin)