cmake_minimum_required(VERSION 3.25)

project(main)

add_executable(${PROJECT_NAME})
target_sources(
        ${PROJECT_NAME}
        PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}/${PROJECT_NAME}.cpp
)

if((NOT DEFINED CMAKE_INSTALL_PREFIX) OR (CMAKE_INSTALL_PREFIX STREQUAL "") OR (CMAKE_INSTALL_PREFIX STREQUAL "/usr/local"))
    message(FATAL_ERROR "CMAKE_INSTALL_PREFIX Is required for this project to be installed correctly!")
else()
    message("CMAKE_INSTALL_PREFIX IS: ${CMAKE_INSTALL_PREFIX}")
endif()

install(TARGETS ${PROJECT_NAME}
        DESTINATION bin
)