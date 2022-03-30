cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(HelloWorld VERSION 1.0)

add_library(
    say_hello
    src/hello.hpp
    src/hello.cpp
)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(HelloWorld PUBLIC say_hello)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_20)
