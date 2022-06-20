cmake_minimum_required(VERSION 3.5)

project(glad)

set(GLAD_LIB_TYPE "STATIC")
if(GLAD_BUILD_SHARED)
	set(GLAD_LIB_TYPE "SHARED")
elseif(GLAD_BUILD_OBJECT)
	set(GLAD_LIB_TYPE "OBJECT")
endif()

add_library(${PROJECT_NAME} ${GLAD_LIB_TYPE} src/glad.c)
target_compile_options(${PROJECT_NAME}  PRIVATE -fPIC)

target_include_directories(
	${PROJECT_NAME}
	PUBLIC include
)

