# glfw
option(GLFW_BUILD_DOCS OFF)
option(GLFW_BUILD_TESTS OFF)
option(GLFW_BUILD_EXAMPLES OFF)
option(GLFW_INSTALL OFF)
add_subdirectory(glfw)

# glm
add_library(glm INTERFACE)
set(GLM_DIR ${CMAKE_CURRENT_SOURCE_DIR}/glm)
target_sources(glm INTERFACE ${GLM_DIR}/glm/glm.hpp)
target_include_directories(glm INTERFACE ${GLM_DIR})

# stb
add_library(stb INTERFACE)
target_include_directories(stb INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/stb")

# tinyobjloader
add_library(tinyobjloader INTERFACE)
target_include_directories(tinyobjloader INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/tinyobjloader")