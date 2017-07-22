add_subdirectory(src)
file(GLOB inc "inc/*.h")
file(COPY ${inc} DESTINATION ${CMAKE_BINARY_DIR}/inc)
