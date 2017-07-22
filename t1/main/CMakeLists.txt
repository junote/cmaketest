AUX_SOURCE_DIRECTORY(. MAIN_SRCS)
ADD_EXECUTABLE(helloworld ${MAIN_SRCS})
target_link_libraries(helloworld hello world)


