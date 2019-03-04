cmake_minimum_required(VERSION 3.10.0)
project(demo)

set(MESSAGE "Demo string")
CONFIGURE_FILE("gen.cpp.in" "gen.cpp" @ONLY)
add_executable(demo ${CMAKE_BINARY_DIR}/gen.cpp main.cpp)
