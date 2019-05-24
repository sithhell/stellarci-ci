cmake_minimum_required(VERSION 3.10)
project(test CXX)

find_package(Boost)

add_executable(a a.cpp)
add_executable(b b.cpp)

enable_testing()

add_test(NAME a COMMAND $<TARGET_FILE:a>)
add_test(NAME b COMMAND $<TARGET_FILE:b>)
