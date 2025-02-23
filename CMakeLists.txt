cmake_minimum_required(VERSION 3.14)
project(iinfo)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Dependencies
set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake ${CMAKE_MODULE_PATH})

find_package(finder REQUIRED)

# library
add_library(${PROJECT_NAME} STATIC no_source.cpp)

target_link_libraries(${PROJECT_NAME} PUBLIC finder)

target_include_directories(${PROJECT_NAME} PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
)