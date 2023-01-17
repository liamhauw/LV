set(TARGET_NAME main)

add_executable(${TARGET_NAME} main.cpp)

add_dependencies(${TARGET_NAME} glsl2spirv)

target_include_directories(
  ${TARGET_NAME} PUBLIC
  ${Vulkan_INCLUDE_DIRS}
)

target_link_libraries(
  ${TARGET_NAME} PUBLIC
  ${Vulkan_LIBRARY} 
  glfw 
  glm 
  stb 
  tinyobjloader 
)