cmake_minimum_required(VERSION 3.10)
project(mingl)

set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE MINGL_SRC src/*)
file(GLOB_RECURSE MINGL_HEADERS include/*)
add_library(mingl ${MINGL_SRC} ${MINGL_HEADERS})
target_include_directories(mingl PUBLIC include)

target_link_libraries(mingl GL)
target_link_libraries(mingl GLU)
target_link_libraries(mingl glut)
