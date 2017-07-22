cmake_minimum_required(VERSION 2.8)
project(helloworld)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
# Add header file include directories
include_directories(${PROJECT_SOURCE_DIR}/inc)
LINK_DIRECTORIES(${PROJECT_BINARY_DIR}/lib)
# Add block directories
add_subdirectory(src)
add_subdirectory(main)
