# 1. Create Source and CMakeFiles.txt
# 2. mkdir build && cd build
# 3. cmake .. - Generating build files/Configure the project
# 4. cmake --build .
# 5. ./Executable

cmake_minimum_required(VERSION 3.22)

project(cmake_practice VERSION 1.0.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD          11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS        OFF)

set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

option(COMPILE_LIBRARIES "Do we want to compile all libraries ?" ON)

if(COMPILE_LIBRARIES)
     add_subdirectory(lib)
else()
    message("ALL Libraries will be recompliled...")
endif()

add_subdirectory(app)


