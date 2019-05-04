cmake_minimum_required (VERSION 3.0)

# Set ARM compiler
SET(PITOOLS_PATH 
/home/viacheslav/PiProject/tools/arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf)

SET(CMAKE_C_COMPILER ${PITOOLS_PATH}/bin/arm-linux-gnueabihf-gcc)
SET(CMAKE_CXX_COMPILER ${PITOOLS_PATH}/bin/arm-linux-gnueabihf-gcc)

# Name our project
project (Hello_world)

include_directories(inc/)

# Add all the *.c files in our source directory to our executable output
FILE(GLOB SRC_FILES 
                    src/*.cpp
                    src/*.c)
add_executable(Hello_world ${SRC_FILES})
