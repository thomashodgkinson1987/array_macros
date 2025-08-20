# Define the minimum CMake version
cmake_minimum_required(VERSION 3.10)
 
# Define the project name
project(array_macros LANGUAGES C)
 
# This is the key part for a header-only library.
# It creates a "virtual" library target. It doesn't compile anything.
# It just tells CMake that this target exists and its public property
# is that its include directory should be used by anyone who links to it.
add_library(array_macros INTERFACE)
 
target_include_directories(array_macros
    INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
