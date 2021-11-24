cmake_minimum_required(VERSION 3.10)

set (CMAKE_CXX_STANDARD 11)

project(HelloHeader)

file(GLOB THIS_LIBRARY
    ./include/foo/*.hpp
    ./src/src.cpp
)

add_library(libMy ${THIS_LIBRARY})

include_directories("./include/")
add_executable(HelloHeader "./src/main.cpp")
target_link_libraries(HelloHeader libMy)


