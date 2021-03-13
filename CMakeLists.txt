cmake_minimum_required(VERSION 3.16)

set(CMAKE_TOOLCHAIN_FILE ${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake
  CACHE STRING "Vcpkg toolchain file")

project(vcpkg_test)

find_package(glfw3 CONFIG REQUIRED)
find_package(fmt CONFIG REQUIRED)

message(STATUS "FOUND GLFW: ${glfw3_FOUND}")
message(STATUS "FOUND FMT: ${fmt_FOUND}")

add_executable(main main.cpp)
target_link_libraries(main PRIVATE fmt::fmt)
