cmake_minimum_required(VERSION 2.8)
project(helloworld)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
SET(CMAKE_SYSTEM_NAME Linux)
# specify the cross compiler
SET(CMAKE_C_COMPILER   /usr/bin/arm-linux-gnueabihf-gcc)
#SET(CMAKE_C_COMPILER   /opt/eldk-2007-01-19/usr/bin/ppc_74xx-gcc)
#SET(CMAKE_CXX_COMPILER /opt/eldk-2007-01-19/usr/bin/ppc_74xx-g++)

# where is the target environment 
#SET(CMAKE_FIND_ROOT_PATH  /opt/eldk-2007-01-19/ppc_74xx /home/alex/eldk-ppc74xx-inst)

# search for programs in the build host directories
SET(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
# for libraries and headers in the target directories
SET(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
SET(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)
ADD_EXECUTABLE(helloworld main.c)
