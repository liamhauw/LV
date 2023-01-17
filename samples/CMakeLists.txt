set(TARGET_NAME main)

add_executable(${TARGET_NAME} main.cpp)

add_dependencies(${TARGET_NAME} glsl2spirv)

target_link_libraries(
  ${TARGET_NAME} PUBLIC
  vulkan
  glfw 
  glm 
  stb 
  tinyobjloader 
)