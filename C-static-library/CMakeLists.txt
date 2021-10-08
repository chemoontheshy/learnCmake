# Set the munimum version of CMake that can be used
cmake_minimum_required(VERSION 3.5)

# Set the project name
project(hello)

# Output path
# Shared
# SET(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/hello/lib )
# static
SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/3rd/lib )

# Add library
add_library(hello STATIC
	src/Hello.cpp
)

target_include_directories(hello
	PUBLIC
		${PROJECT_SOURCE_DIR}/include
)

file(COPY ${PROJECT_SOURCE_DIR}/include DESTINATION  ${PROJECT_SOURCE_DIR}/3rd/)




