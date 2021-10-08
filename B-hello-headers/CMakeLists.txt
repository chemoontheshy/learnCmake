# Set the munimum version of CMake that can be used
cmake_minimum_required(VERSION 3.5)

# Set the project name
project(hello_headers)

# Output path
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin )

# Add .cpp
SET(SOURCES 
	src/Hello.cpp
	src/main.cpp)

#Add an executalble
add_executable(hello_headers ${SOURCES})

#include .h
target_include_directories(hello_headers
	        PRIVATE
		       ${PROJECT_SOURCE_DIR}/src 
)




