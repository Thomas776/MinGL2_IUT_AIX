cmake_minimum_required(VERSION 3.10)
project(mingl)

set(CMAKE_CXX_STANDARD 17)
set(BUILD_SHARED_LIBS yes)

file(GLOB_RECURSE SRC src/*)
file(GLOB_RECURSE HEADERS include/*)
add_library(mingl ${SRC} ${HEADERS})
target_include_directories(mingl PUBLIC include)


target_link_libraries(mingl GL)
target_link_libraries(mingl GLU)
target_link_libraries(mingl glut)
