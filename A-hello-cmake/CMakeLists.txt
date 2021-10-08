#Set the munimum version of CMake that can be used
cmake_minimum_required(VERSION 3.5)

#set the project name
project (hello_cmake)

SET(SOURCES src/main.cpp)

#Add an executalbe
add_executable(hello_cmake ${SOURCES})

#Output path
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
