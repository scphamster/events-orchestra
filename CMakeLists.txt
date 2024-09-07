cmake_minimum_required(VERSION 3.25)

project(simple
        DESCRIPTION "Simple c++ project for bitbake integration test"
)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

add_subdirectory(src)