cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(HelloWorld VERSION 1.0)

set(my_bool TRUE)

if(my_bool)
    message(STATUS "Condition was met")
else()
    message(STATUS "Condition failed")
endif()

add_subdirectory(say-hello)
add_subdirectory(hello-exe)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_20)
