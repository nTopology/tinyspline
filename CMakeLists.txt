cmake_minimum_required(VERSION 3.10)

if(WIN32)
  #set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /wd4244")
  #set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /wd4267")
endif()

### Sources ###

set(sources
    src/tinyspline.c
    src/tinyspline.h
    src/tinysplinecpp.cpp
    src/tinysplinecpp.h
)

# This corrects cmake's default Visual Studio's ugly folder organization
source_group("" FILES ${sources})

add_library(tinyspline ${sources})

target_include_directories(tinyspline PUBLIC src)

#target_link_libraries(tetwild PUBLIC
#  glm geogram libigl2 cgal2)
