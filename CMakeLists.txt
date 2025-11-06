cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
set(CMAKE_CXX_STANDARD 17) 

set(PROJECT_NAME tgAnswer)

project(${PROJECT_NAME})

find_package(Td 1.8.56 REQUIRED)

add_executable(${PROJECT_NAME} main.cpp TdObject.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE Td::TdStatic)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})