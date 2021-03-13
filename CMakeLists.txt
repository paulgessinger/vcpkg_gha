cmake_minimum_required(VERSION 3.16)
project(vcpkg_test)

find_package(glfw3 CONFIG REQUIRED)

message(STATUS "FOUND: ${glfw3_FOUND}")
