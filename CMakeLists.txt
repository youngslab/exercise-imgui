

cmake_minimum_required(VERSION 3.10)

project(exercise-imgui)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_BINARY_DIR}
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

find_package(glfw REQUIRED)
find_package(glm REQUIRED)
find_package(glad REQUIRED)
find_package(imgui REQUIRED)

add_executable(exercise-imgui
	main.cpp
	imgui_impl_glfw.cpp
	imgui_impl_opengl3.cpp)

target_link_libraries(exercise-imgui
	glfw::glfw
	glad::glad
	glm::glm
	imgui::imgui)
