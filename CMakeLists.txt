cmake_minimum_required(VERSION 3.16)

project(hello_world C)

add_executable(hello hello.c)

if (CMAKE_C_COMPILER_ID MATCHES "Clang|GNU")
  target_compile_options(hello PRIVATE -Wall -Wextra -Wpedantic)
elseif (MSVC)
  target_compile_options(hello PRIVATE /W4)
endif()
