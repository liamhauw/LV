cmake_minimum_required(VERSION 3.20...3.25)

project(
  LV
  VERSION 0.1.0
  LANGUAGES CXX C
)

list(APPEND CMAKE_MODULE_PATH
  ${CMAKE_CURRENT_SOURCE_DIR}/bldsys/cmake
)

include(global_options)
include(setup_vulkan)

add_subdirectory(third_party)
add_subdirectory(shaders)
add_subdirectory(samples)