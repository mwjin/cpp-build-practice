# CMake 프로그램의 최소 버전
cmake_minimum_required(VERSION 3.11)

# 프로젝트 정보
project(
    CMakePractice
    VERSION 0.1
    DESCRIPTION "Practice building C++ project"
    LANGUAGES CXX)

add_executable(program src/main.cpp src/foo.cpp src/bar.cpp)
target_compile_options(program PUBLIC -std=c++17 -g -Wall -Werror)
target_include_directories(program PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_sources(program PUBLIC)
