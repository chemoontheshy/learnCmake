# Set the munimum version of CMake that can be used
cmake_minimum_required(VERSION 3.5)

# Set the project name
project(hello_shared)

# Output path
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

SET(3RD ${PROJECT_SOURCE_DIR}/3rd)

# link include
INCLUDE_DIRECTORIES(${3RD}/include)

# link lib
LINK_DIRECTORIES(${3RD}/lib)


# Add an executable with the above sources
add_executable(hello_shared
	src/main.cpp
)

target_link_libraries(hello_shared hello)






