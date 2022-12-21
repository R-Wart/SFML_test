cmake_minimum_required(VERSION 3.24)
project(SFML_test)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXE_LINKER_FLAGS "-static")

add_executable(SFML_test main.cpp)

set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR C:/msys64/mingw64/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio REQUIRED)

target_link_libraries(SFML_test sfml-system sfml-window sfml-graphics sfml-audio)