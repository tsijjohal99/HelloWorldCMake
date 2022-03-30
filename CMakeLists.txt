cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(HelloWorld VERSION 1.0)

set(MY_STRING "This is a string")
set(MY_OTHER_STRING "This is a string")
set(my_value 4)

foreach(idx RANGE 0 99 5)
    message(STATUS "Item is: ${idx}")
endforeach()

add_subdirectory(say-hello)
add_subdirectory(hello-exe)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_20)
