cmake_minimum_required(VERSION 3.5.1)
project(controller)

set(SOURCE_FILES
	src/controller.cpp
)

add_library(controller STATIC ${SOURCE_FILES})

include_directories(
	${CMAKE_SOURCE_DIR}/src/util/include
)

target_include_directories(controller PUBLIC
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)
