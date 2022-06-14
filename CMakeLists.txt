cmake_minimum_required(VERSION 3.5)

project(glad)

add_library(${PROJECT_NAME} STATIC src/glad.c)
target_compile_options(${PROJECT_NAME}  PRIVATE -fPIC)

target_include_directories(
	${PROJECT_NAME}
	PUBLIC include
)
