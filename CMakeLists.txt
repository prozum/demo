cmake_minimum_required(VERSION 3.10.0)
project(demo)

set(MESSAGE "Generated string")
CONFIGURE_FILE("gen.cpp.in" "gen.cpp" @ONLY)
add_library(src ${CMAKE_BINARY_DIR}/gen.cpp)
add_library(gen src.cpp)
add_executable(main main.cpp)
target_link_libraries(main src gen)
