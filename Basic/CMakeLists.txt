# 1. Create Source and CMakeFiles.txt
# 2. mkdir build && cd build
# 3. cmake .. - Generating build files/Configure the project
# 4. cmake --build .
# 5. ./Executable

cmake_minimum_required(VERSION 3.22)

project(
    cmake_practice
VERSION 1.0.0
LANGUAGES C CXX)

add_library(Library STATIC mylib.cpp)
add_executable(Executable main.cpp)

target_link_libraries(Executable PUBLIC Library)