cmake_minimum_required(VERSION 3.10)

project(dsacpp)

if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

message(STATUS "CMAKE BUILD TYPE: ${CMAKE_BUILD_TYPE}")

# set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "-std=c++17 -pthread -fPIC")

set(CURRENT_FOLDER ${CMAKE_CURRENT_SOURCE_DIR})
message(STATUS "CMAKE BUILD FLODER: ${CURRENT_FOLDER}")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CURRENT_FOLDER}/bin)

add_executable(gcd gcd/main.cpp)
