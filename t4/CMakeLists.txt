cmake_minimum_required(VERSION 2.8)
project(libs)

SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
include_directories(${PROJECT_SOURCE_DIR}/inc ${PROJECT_BINARY_DIR}/inc)
LINK_DIRECTORIES(${PROJECT_BINARY_DIR}/lib)

file(GLOB fileFold "*")
foreach(fileFoldName ${fileFold})
    get_filename_component(VarName ${fileFoldName} NAME)
    #add if for except build
    set(inc "${fileFoldName}/inc/*.h")

    file(GLOB inc ${inc})
    file(COPY ${inc} DESTINATION ${CMAKE_BINARY_DIR}/inc)
    set(src "${fileFoldName}/src/*.c")
    file(GLOB src ${src})
    add_library(${VarName} SHARED ${src})
endforeach(fileFoldName)

