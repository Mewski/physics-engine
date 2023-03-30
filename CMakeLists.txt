cmake_minimum_required(VERSION 3.25)

project(physics-engine)

set(CMAKE_CXX_STANDARD 23)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -static")

add_library(physics-engine STATIC
  src/utilities.cpp

  include/utilities.h
)

add_executable(physics-engine-app
  src/main.cpp
)

target_link_libraries(physics-engine-app
  physics-engine
)